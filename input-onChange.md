![](https://media.giphy.com/media/7ezJodj5j9vCOduwUU/giphy.gif)
```js
function App() {
  const [user, setUser] = useState<string>('');

  return (
    <div>
      <h1>
        <input onChange={event => setUser(event.target.value)}></input>
      </h1>
      <h2>
      <input value={user}></input>
      </h2>
    </div>
  );
}
```
## Use cases  
1. Spelling checker  
2. Account validation
3. Input tracker
