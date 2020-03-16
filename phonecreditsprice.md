### Get the phone credits price

method : GET

What you need :
- prefix number (0819,0821,0838,0856, etc)
- access_token
>you can get access_token from reqtoken

```
curl "https://api.bukalapak.com/phone-credits/prepaid-products/?prefix=08191&access_token=youraccesstoken"
```

response you need is all data from body response