![](https://media.giphy.com/media/Df5JQeKtHFlaoLSu4d/giphy.gif)

```js
function App() {
  const [user, setUser] = useState<string>('');
  const myStyle = {
    width: '300px',
  }
  let boi = "kratos's calling atreus";
  const UserHandler = () => {
    setUser(boi);
  }

  return (
    <div>
      <h1>
        
        <button onClick={() => setUser(boi + ' but with functional form')}>Set with functional form</button>
        <button onClick={UserHandler}>Set with declarative form</button>
      </h1>
      <h2>
      <input style={myStyle} value={user}></input>
      </h2>
    </div>
  );
}
```
## Use cases  
1. Form options  
2. Button Event Trigger
3. More on this later!
