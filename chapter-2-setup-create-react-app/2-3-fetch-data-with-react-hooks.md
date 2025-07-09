# Chapter 2 - Setup: Create React App
## Lesson 3 - Fetch Data with React Hooks

Next, lets learn how to fetch data with React from an online API.<br>
URL [Orange Valley Videos API](https://orangevalleycaa.org/api/videos)

If you open the url in a web browser it will display an object with insight into the data fields, which are displayed below. These properties will help us to focus on which data we want to use from the request to this API.

    id, video_url, name, description, duration, created_by, 
    image, thumbnail, cropped, file_name_original, popularity,
    category_id, category, keywords

If you want to test this is your browser you can grab a piece of the data. For example you can find the video with an "id" of 1 with a "video_url" of https://orangevalleycaa.org/api/videos/WomanSculpsClayMusic_042009083.mp4". Opening this is a browser autoplays the video. This helps prove this data is available for us via the API.

In React, the hooks *useState* and *useEffect* will be used to store some state in our app and to execute some code after the React App component renders.

First, the *useState* Hook will create a state variable named "data" with a setter function called "setData". The initial value is an empty array []. React hooks must be used inside the body of a component. In this case we are using the App component (src/App.jsx).

[App.jsx]
<pre><code>
import { useState, setState } from 'react';
import './App.css';

function App(){
  const [data, setData] = useState([]);
  return (
    ...
  )
}
</code></pre>

Next, the *useEffect()* hook will help with data fetching. The function we pass to this hook will happen after the render. Create a callback function inside of *useEffect*. Within the callback create a new **async** function called "fetchData" that will make a http request for the data in the API using the browser's *Fetch API*.<br>
The useEffect() function takes a second argument which is a list or dependencies & we specify an empty array to tell this effect to run ONCE.<br>
The *async* keword denotes a function making an asyncronous request.<br>
The *await* keyword will wait until the response is finished before it continues.<br>
NOTE: The instructor uses "await fetch(...).then(response.json())" but using the syntax below with "await" is also fine.

[App.jsx]
<pre><code>
import { useState, setState } from 'react';
import './App.css';

function App(){
  const [data, setData] = useState([]);

  useEffect(() => {
    const fetchData = async ()=> {
      const result = await fetch('https://orangevalleycaa.org/api/videos');
      const result_json = await result.json();
      setData(result_json);
    }
    fetchData();
  }, []);

  return (
    &lt;div className="App">
      &lt;header>
        &lt;h1>Videos&lt;/h1>
      &lt;/header>
    &lt;/div>
  )
}
</code></pre>

Next we want to be able to use the fetched data by adding some JSX and take advantage of JavaScript's map() method to loop through the results to determine which parts of the response we want to display.

[App.jsx]
<pre><code>
import { useState, setState } from 'react';
import './App.css';

const api_url = 'https://orangevalleycaa.org/api/videos';

function App(){
  const [data, setData] = useState([]);
  
  useEffect(() => {
    const fetchData = async ()=> {
      const result = await fetch(api_url);
      const result_json = await result.json();
      setData(result_json);
    }
    fetchData();
  }, []);

  return (
    &lt;div className="App">
      &lt;header>
        &lt;h1>Videos&lt;/h1>
      &lt;/header>
      {data.map(video => (
        &lt;div key={video.id}>
          &lt;h2>{video.name}&lt;h2>
          &lt;video height={200} controls src={video_url} />
        &lt;/div>
      ))}
    &lt;/div>
  )
}
</code></pre>


If all went well you should see your React app now renders multiple movies, each within a div with a title.
