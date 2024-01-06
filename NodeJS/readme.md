## NodeJS, Runtime and more.

**JavaScript (JS)** can be executed in different environments such as web browsers, and one popular environment for running JavaScript on a machine is **Node.js**

Nodejs is a runtime env (short for environment) created by some people and launched in 2009. It allows javascript to run on the backend.

It was created on the top of v8 engine (engine that runs javascript inside chromium based browsers)

## What is a runtime env?

A runtime environment is a software framework that provides the necessary resources and services for the execution of application.

It includes components such as **libraries, APIs and tools**, etc that allows software to run and operate on a computer or within a specific platform.

Think of runtime as kitchen and the food recipe as programming language.

## Nodejs history?

**Nodejs** is a runtime env created by a bunch of smart people who took out **v8 engine** from the **chromium** and added some extra backend features to make it a competitor for languages like **java** which used to be a very powerful backend language.

**Nodejs** creators wanted to make an ecosystem for javascript that can be used to create both frontend and backend applications.

So Nodejs = **v8 engine + apis + core modules like fs, path, etc.**

## What can you do with nodejs?

- CLIs
- Videoplayers
- Games
- HTTP Servers and more.

## Comparing it with Java Runtime Environment

|  | Java Runtime Env | Nodejs |
| --- | --- | --- |
| **Primary use** | Running java apps on client and server side | Running JS on server side |
| **Compiler** | JVM (Java Virtual Machine) | V8 engine from Chromium |
| **Compiled code** | Typically compiled to bytecode | Interpreted to machine code|
| **Language** | Java | JavaScript |
| **Package manager** | Gradle, Maven | npm, pnpm |
| **Popular Backend Frameworks** | Spring, Hibernate, Apache | Express, Nest |

## What is Bun?

Bun is a competitor to nodejs, they are trying to make bun faster compared to nodejs. 

Also bun is fully backward compatible which means any bun code is also nodejs code or vice versa. It is created using zig programming language which is used in low latency systems.

## How to run code with nodejs

```jsx
node index.js
```