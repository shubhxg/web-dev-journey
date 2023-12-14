## Loops 

- For loop
- While loop
- Nested for and while loop

```jsx
for (initialization; condition; iteration) {
	//do this
}

//initialization happens at the top in while loops;

var i=1;
while (condition) {
	// do this
	increment
}

for (i, c, i++) { //----------------------> outer loop
	// do this before second loop
	for (i, c, i++) { //---------------------> inner loop
		//do this
	}
}
```
