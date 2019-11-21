A pipeline checking if a secret with a provided id has expected username and password values.

```   
    parameters([
        string(name:'SECRETID', description:'ID of the secret'),
        string(name:'EXPECTEDUSER', description:'Name of the user'),
        string(name:'EXPECTEDPWD', description:'Password of the user')
    ])
```
