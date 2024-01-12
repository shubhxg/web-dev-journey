## Sending status codes to the client
We can send status codes via response from server.

```jsx
app.post('/', (req, res) => {
    res.sendStatus(200);
})

app.get('/wrongRoute', (req, res) => {
    res.sendStatus(404);
})
```