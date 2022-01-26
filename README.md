## Sending Get Request to Another Backend API

### General information

In order to facilitate making HTTP requests to external services, we create the **request()** method. The **request()** method takes two arguments; it takes a configuration object containing details about the request as well as a callback to handle the response. Therefore, next we create variables **options** and **request** as part of **handleGetRequest** function. Next, our HTTP request needs to be set up to be able to receive the data properly. Data from the response will usually be received in chunks and pieced together. As such, we need to watch for these chunks of data and process them. We can do this by listening to the data event.
In the callback of the **.request()** method, we create a variable called **data** initialized with an empty string. Then, listen for the data event and add the received data to the **data** variable. Once all of the data has been received from the response, we need to handle that data.
To know when a response is finished, we can listen for the end event. Still in the callback of the **.request()** method, we set up a listener for the end event of the response using **response.on()**  method and adding **end** event as first argument. When the **end** event is triggered, we can work with the data from the response.

### Tools used 

+ JavaScript
+ VS
+ node.js
+ command line
