### Login to bukalapak
method: POST

what you need:
- username and password
- header request
- identity
- authenticity token

for http header request,
you must login manually to bukalapak web, copy header request then add to cURL.

>you can get identity token from data-identity at html tag contain https://www.bukalapak.com/track_external.json

example :
```
<div class="js-siburung-track-hook u-hidden hidden" data-identity="71082de2f6fe4321dsa5903fbe8be83">https://www.bukalapak.com/track_external.json</div>
```
>you can get authencity token from name="csrf-token" at html tag as content 

example :
```
<meta name="csrf-token" content="UJPpqfPeMRfuLCdWetC5x+cNsNt+jPUXt8YRg02hGqFPvj0FhZ54JrbWPLYgKojQoNQ/h/rvuln8AQsVw==">
```

```
curl "https://www.bukalapak.com/user_sessions" -H "User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:74.0) Gecko/20100101 Firefox/74.0" -H "Accept: */*" -H "Accept-Language: en-US,en;q=0.5" --compressed -H "X-NewRelic-ID: VQcDWF9ADgIJVVBQ" -H "X-CSRF-Token: d2lMgvgZMyACzmTncoD5AAtoaaH60jfxQJoB1l2PclYRfs+uNT/2IfqboyvTCLIdFQDdzOW0CoNRFzzvcpMYDA==" -H "Content-Type: application/x-www-form-urlencoded; charset=UTF-8" -H "X-Requested-With: XMLHttpRequest" -H "Origin: https://www.bukalapak.com" -H "Connection: keep-alive" -H "Referer: https://www.bukalapak.com/login?comeback="%"2Fusers"%"2Fsecret&flash=" -H "Cookie: __cfduid=d8baf708ddcfc82794bde668a02da20211584267017; _gcl_au=1.1.1310840147.1584267017; _vwo_uuid_v2=DA923EFE153D6C70541990FB189977275|0de9d47f5398ff09f536481261d08f4a; _ga=GA1.2.1266226775.1584267022; _fbp=fb.1.1584267026665.1715110025; kppid_managed=kppidff_NSOG6CU1; identity=71082de2f6fe4589267d5903fbe8be83; browser_id=79e54312ae3807e9624e090c8e41d27b; __cfruid=41167225443f98cd918a0579aff75453056d7031-1584364188; __auc=2ea74065170e376f90780cea6a4; session_id=0d9e409823d7b187e4cf80304d0480d9; lskjfewjrh34ghj23brjh234=T3RIamp4bWl5eWNhcVpaOE1ZSkRyZllhTWd2NjFyb3E5S3N1VTZ3ZjJtR0N3dE9vM05yRDVma0FKWGdnVHhHWEtNTFN3OE90SHRsajRGTWlCYjhmQnhWemdXQlVJYTBJakRtK01tcXkzdkJjVnM1dmVQVk5UcUs4MGJMRE9ORmZJQzVYbjJyQ0UvTkNMbms3NGc2WXpkaTRkUGU2VncxK1hYMllxQjNqZmlsNG9OaXhTUWIvWkk3SnM5Q2Z5czNDRXB0bUNpU3p0RDgzTXM1TlJDK1FGWCsxUzZmY2JSSFNNVlI3bW9HMWVzaEZFZzRVNnh4YVUvTWRjaHBpMy9NQTI5azdrWnFobFpzVEZsSGlHWnNVYXc9PS0taEhDOUZPdm9wRUVRTytxVThMb0pqUT09--dd4929d5ef6ea6ec41de48d2f823fb255d46936c; _gid=GA1.2.980798093.1584364193; _gat=1; __asc=d825e3d7170e3789d57dd698b79; _td=b846b3c5-9d6a-4e50-ca06-954f6b86cd11" -H "Pragma: no-cache" -H "Cache-Control: no-cache" -H "TE: Trailers" --data "user_session"%"5Busername"%"5D=YOURUSERNAME&user_session"%"5Bpassword"%"5D=YOURPASSWORD&user_session"%"5Bremember_me"%"5D=1&identity=71082de2f6fe4589267d5903fbe8be83&authenticity_token=d2lMgvgZMyACzmTncoD5AAtoaaH60jfxQJoB1l2PclYRfs"%"2BuNT"%"2F2IfqboyvTCLIdFQDdzOW0CoNRFzzvcpMYDA"%"3D"%"3D&comeback="%"2Fusers"%"2Fsecret"
```
response what you need is otp_key from body response