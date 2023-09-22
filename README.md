## LOGIN API (～￣▽￣)~

-   *Requirements*
> 1. UUID
> 2. A server to send POST requests! 

- ### Example Curl Request
>  `curl -i -X POST -H "Content-Type: application/json" -d '{"uuid": "0051d59a-5257-4d05-8cf2-16f1b85ec0814", "qr_id": "string"}' http://xx.xx.xxx.xxx:5000/login` 


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

- ***This Request opens up the WhatsApp portal in the main server using selenium and searches for the search bar in the WhatsApp which only comes if the login is done somehow so it confirms if the login is done or not. ***


******************************************************************************

## Sending Messages (●'◡'●)


-   *Requirements*
> 1. UUID
> 2. A server to send POST requests! 
> 3. Receiver's Number ('+911231231212') *international format*
> 4. Attach = True/False
> 5. Attachment Url (only if attach = true)
> 6. Type (only if attach = true)

- **IF ATTACH=FALSE**

  `curl -X POST -H "Content-Type: application/json" -d '{"text": "i am sick so low ass testing", "uuid": "0051d59a-5257-4d05-8cf2-16f1b85ec0812"}' "http://xxxxxxxxxxx:5001/send_message?phone=+919922278312&attach=false"`

*AS you can see here phone number of the reciever , attach parameter , uuid and message are getting passed through the server*

- **IF ATTACH=TRUE**

`curl -X POST -H "Content-Type: application/json" -d '{"text": "i am sick so low ass testing", "uuid": "0051d59a-5257-4d05-8cf2-16f1b85ec071" , "attachment_url": "https://yog-whatsapp-files.s3.ap-south-1.amazonaws.com/attachments/fde83688-e9cd-44bd-bda8-ed7462fc2038/dummy.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAZ74A2IE32PV7P5WC%2F20230914%2Fap-south-1%2Fs3%2Faws4_request&X-Amz-Date=20230914T154935Z&X-Amz-Expires=604800&X-Amz-Signature=d48ed610f5e0dfac1172809f7ae621507a86c49ef49755ff9995e3fe0129d283&X-Amz-SignedHeaders=host"}' "http://xxx .xxx .xxx .xxx:5001/send_message?phone=+913121231212&attach=true&type=pdf"
`

*As you can see here phone number of the receiver , attach parameter , attach file type , attachment url , text message , uuid are getting passed into the server. see do not give wrong parameter for attach=true&type=image or type=pdf* 

- any other parameter will be rejected by the server  


- Good Respnse For Both Of The Requests

 ```
{
  "phone": " 91991112226",
  "status": "Message sent successfully",
  "text": "i am sick so low ass testing"
}

```
## Logmeout (≧∇≦)


-   *Requirements*
> 1. UUID

- *Example Request khikhikhi*

`curl -X POST -H "Content-Type: application/json" -d '{"uuid": "0051d59a-5257-4d05-8cf2-16f1b85ec070"}' http://xx.xxx.xxxxx.xxxxxxx/logmeout
`
- Good Respnse For logout

 ```
{
  "logout": "true"
}

note - "logout": "false" would be for any other conditions 
```
