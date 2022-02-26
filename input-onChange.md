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
