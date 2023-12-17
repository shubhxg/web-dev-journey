## Date and time

`variable = new Date();` → returns date in a weird string 

so we can use `toString() or toLocaleString() or toLocaleDateString()`; etc to convert it into human readable format.

**Getting time of any country**

```jsx
 
const dateNew = new Date().toLocaleString('en-US',{timeZone: 'Asia/Kolkata'};
```

The first argument is the locale string ('en-US'), and the second argument is an options object (`timezoneForAsia`).

There are more methods such as: 

- `now()`
- `getDate()`
- `getDay()` ...