### Req Token
method: POST

What you need :
- application id
- authenticity token
>you can get application id from id="application_id" after you log in

example :
```
<input type="hidden" name="application_id" id="application_id" value="231d4a86905f0f262c5dsad">
```

>you can get authenticity token from same form with application id or you can use login authenticity token. but you must convert it to url encode
example:
```
%2BAwWZPxvZypGyQtawe3yIFkd7raadK%2FDWe%2B%2FqHvn7tGeG5VIMUmiK76czJZgZbk9R3Va24USkrFIYoKRVPuEiw%3D%3D
```

```
curl "https://www.bukalapak.com/auth_proxies/request_token" --data "application_id=231d4a86905f0f262c5dsad&authenticity_token="%"2BAwWZPxvZypGyQtawe3yIFkd7raadK"%"2FDWe"%"2B"%"2FqHvn7tGeG5VIMUmiK76czJZgZbk9R3Va24USkrFIYoKRVPuEiw%3D"%"3D"
```
response what you need is access_token from body response


