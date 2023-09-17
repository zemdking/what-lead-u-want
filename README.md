## LOGIN API (～￣▽￣)~

-   *Requirements*
> 1. UUID
> 2. A server to send POST requests! 

- ### Example Curl Request
>  `curl -i -X POST -H "Content-Type: application/json" -d '{"uuid": "0051d59a-5257-4d05-8cf2-16f1b85ec0814"}' http://xx.xx.xxx.xxx:5000/login` 


- **You can make a post request to the server and if the request is successful it will give a response like this**

```

HTTP/1.1 200 OK
Server: Werkzeug/2.3.7 Python/3.11.5
Date: Sun, 17 Sep 2023 14:37:00 GMT
Content-Type: application/json
Content-Length: 28
Connection: close

{"message":"login success"}

```


******************************************************************************


## LOGIN CHECK ヾ(•ω•ヾ)

-   *Requirements*
> 1. UUID
> 2. A server to send POST requests! 


- ### Example Curl Request
>  `curl -i -X POST -H "Content-Type: application/json" -d '{"uuid": "0051d59a-5257-4d05-8cf2-16f1b85ec0814"}' http://xx.xx.xxx.xxx:5002/logincheck` 

- **You can make a post request to the login check server to confirm if the login is successful or not and if the request is successful it will give a response like this**

```

HTTP/1.1 200 OK
Server: Werkzeug/2.3.7 Python/3.11.5
Date: Sun, 17 Sep 2023 14:37:00 GMT
Content-Type: application/json
Content-Length: 28
Connection: close

{"message":"login success"}

or 

{"message":"login failed"}

```

> ***This Request opens up the WhatsApp portal in the main server using selenium and searches for the search bar in the WhatsApp which only comes if the login is done somehow so it confirms if the login is done or not. 


******************************************************************************

## Sending Messages (●'◡'●)


-   *Requirements*
> 1. UUID
> 2. A server to send POST requests! 
> 3. 
