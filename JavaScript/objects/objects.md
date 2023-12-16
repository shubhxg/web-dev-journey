## Object literals

- Objects are collection of key value pairs.
- Objects have different properties which are described in form of key value pairs.
- Key and value both are stored as a string in memory but you do not have to write keys as `"key"` instead just `key:`
- If you want to use a symbol as a key in an object you will need to use square brackets [ ], `[symbolKey]: "value"` otherwise it will take symbol as a string.
- Syntax of an object is:

```jsx
const object1 = {
	key: "value",
	key: true,
	key: [value,value,value],
}
```

- We can even add objects inside objects.

```jsx
const object2 = {
	key: value,
	key: "value",
	objectInsideObject: {
		key: value,
		key: "value"
	}
}
```

- Accessing values from objects
    - `object.property`
    - `object["key"]`
    - `object["key"]["key2"]...`
- Adding new property to the object.
    - `object.property = value;`
    - `object["key"] = value`

## Array of objects = [{ : }]

- We can create arrays of objects.

```jsx
const array = [
	{
		key:value, 
		key:value
	},
	{
		key:value,
		key:value
	}
]
```

- To access these objects from the array
    - `array[indexNumber].property;`
    - `array[indexNumber]["key"]...`
- Array of objects are similar to JSON file data which is used to share data between the server and the client side.
- To convert this data into JSON data: `const newObject = JSON.stringify(arrayofObjects);`

## Freezing objects

You can freeze objects in order to make them immutable.

```jsx
Object.freeze(object1);
```
