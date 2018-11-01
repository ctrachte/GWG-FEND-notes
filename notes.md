# XHR Usage Review
##There are a number of steps you need to take to send an HTTP request asynchronously with JavaScript.

To Send An Async Request (AJAX)
1. create an XHR object with the XMLHttpRequest constructor function
2. use the .open() method - set the HTTP method and the URL of the resource to be fetched
3. set the .onload property - set this to a function that will run upon a successful fetch
4. set the .onerror property - set this to a function that will run when an error occurs
5. use the .send() method - send the request

## Example:
```
const searchedForText = 'hippos';
const unsplashRequest = new XMLHttpRequest();

unsplashRequest.open('GET', `https://api.unsplash.com/search/photos?page=1&query=${searchedForText}`);
unsplashRequest.onload = addImage;
unsplashRequest.setRequestHeader('Authorization', 'Client-ID <your-client-id>');
unsplashRequest.send();

function addImage(){
  //do something here with your data
}
```
