### axios
[https://www.npmjs.com/package/axios](https://www.npmjs.com/package/axios)

#### Installing
```
npm install axios --save
```

#### Request method aliases
For convenience aliases have been provided for all supported request methods.
```
axios.request(config)
axios.get(url[, config])
axios.delete(url[, config])
axios.head(url[, config])
axios.options(url[, config])
axios.post(url[, data[, config]])
axios.put(url[, data[, config]])
axios.patch(url[, data[, config]])
```

### Performing multiple concurrent requests
```
function getUserAccount() {
  return axios.get('/user/12345');
}
 
function getUserPermissions() {
  return axios.get('/user/12345/permissions');
}
 
axios.all([getUserAccount(), getUserPermissions()])
  .then(axios.spread(function (acct, perms) {
    // Both requests are now complete 
  }));
```