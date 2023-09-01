# Superhero Hunter

* Created SuperHero search page using html,css and javascript.
* Details are fetched using Marvel API.

### Marvel API

* Register yourself to the above website https://developer.marvel.com/signup and generate the public and private key.
* You need to use the timestamp as ts and then create the hash using md5 hash of ts, private-key and public-key. 
* After generating API Key you can fetch details using different endpoints. Which you can get from  https://developer.marvel.com/docs 

```javascript
var marvelURL = 'http://gateway.marvel.com/v1/public/'
var marvelURLHeader=`ts=1&apikey=${marvelAPI.apiKey}&hash=${marvelAPI.hash}`;

const getdata = async (URL)=>{
    let res = await fetch(URL);
    res = await res.json();
    let data = res.data.results;
    return data;
}
```