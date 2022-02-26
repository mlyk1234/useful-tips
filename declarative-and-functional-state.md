```js
function App() {
  const [user, setUser] = useState<string>('');

  let boi = 'Kratos\'son';
  const UserHandler = () => {
    setUser(boi);
  }

  return (
    <div>
      <h1>
        <input value={boi}></input>
        <button onClick={() => setUser(boi)}>Set with functional form</button>
        <button onClick={UserHandler}>Set with declarative form</button>
      </h1>
      <h2>
      <input value={user}></input>
      </h2>
    </div>
  );
}
```
