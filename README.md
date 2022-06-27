# React-useState
### Basic useState examples


- [x] **Counter (Number)**
```js
import { useState } from 'react';

export default function Counter() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return (
    <button onClick={handleClick}>
      You pressed me {count} times
    </button>
  );
}

```

https://user-images.githubusercontent.com/85023604/175839051-057d59ab-dc5a-40b5-a195-445ecbdda28a.mov

---

- [x] **Text field (String)**

```js
import { useState } from 'react';

export default function MyInput() {
  const [text, setText] = useState('hello');

  function handleChange(e) {
    setText(e.target.value);
  }

  return (
    <>
      <input value={text} onChange={handleChange} />
      <p>You typed: {text}</p>
      <button onClick={() => setText('hello')}>
        Reset
      </button>
    </>
  );
}
```

https://user-images.githubusercontent.com/85023604/175839316-1deb3f07-c9fd-4ccc-a036-2d4ff4093011.mov

---

- [x] **Checkbox (Boolean)**
```js
import { useState } from 'react';

export default function MyCheckbox() {
  const [liked, setLiked] = useState(true);

  function handleChange(e) {
    setLiked(e.target.checked);
  }

  return (
    <>
      <label>
        <input
          type="checkbox"
          checked={liked}
          onChange={handleChange}
        />
        I liked this
      </label>
      <p>You {liked ? 'liked' : 'did not like'} this.</p>
    </>
  );
}

```

https://user-images.githubusercontent.com/85023604/175839632-15dffeda-cd2a-44f4-bbad-481b8770f739.mov

---

- [x] **Form (two variables)**
```js
import { useState } from 'react';

export default function Form() {
  const [name, setName] = useState('Taylor');
  const [age, setAge] = useState(42);

  return (
    <>
      <input
        value={name}
        onChange={e => setName(e.target.value)}
      />
      <button onClick={() => setAge(age + 1)}>
        Increment age
      </button>
      <p>Hello, {name}. You are {age}.</p>
    </>
  );
}

```

https://user-images.githubusercontent.com/85023604/175839899-ed963932-0f35-4e85-9dbe-b02156490c42.mov








