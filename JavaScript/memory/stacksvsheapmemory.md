## Stack vs. Heap memory
- You get a copy of data when it gets stored into the stack memory.
- You get the reference of the original value when it is stored in the heap memory.
- **stack memory** → primitives → immutable
- **heap memory** → non-primitives → mutable
- When you work with a primitive datatypes, any operation that appears to **"modify"** the value is actually creating a new value.
- This is because primitives are **passed by value**, meaning a copy of the actual value is passed around, and changes to the copy don't affect the original value.
- However, when you work with non-primitives such as objects, you are working with references to the actual data rather than the data itself which means **passed by reference**. So the changes you make through one reference will affect the underlying data, impacting other references to the same data.
