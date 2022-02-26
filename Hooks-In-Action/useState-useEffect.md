## Requirements  
# Make sure you understand useState steadily  

Now see useEffect in action on your browser console!

```js
import React, { useState, useEffect } from "react";

export default function App() {
  const [resourceType, setResourceType] = useState("posts");
  const [items, setItems] = useState([]);

  console.log("execute");
  useEffect(() => {
    console.log("resource changed");
    fetch("https://jsonplaceholder.typicode.com/"+resourceType)
      .then((response) => response.json())
      .then((json) => console.log(json));
      
    return () => {
      console.log("return from resource change");
    }; // A cleanup for mount or unmount | watch the console & try reclick the button
  }, [resourceType]);
  
  return (
    <>
      <div>
        <button onClick={() => setResourceType("posts")}>Posts</button>
        <button onClick={() => setResourceType("users")}>Users</button>
        <button onClick={() => setResourceType("comments")}>Comments</button>
      </div>
      <h1>{resourceType}</h1>
    </>
  );
}
```
