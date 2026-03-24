fetch('https://jsonplaceholder.typicode.com/users')
.then(response => response.json())
.then(data => console.log(JSON.stringify(data, null, 2)))
.catch(error => console.error(error));
