# ShoonyaApi
# Shoonya Python Api

Copy files in your project
```
!wget https://raw.githubusercontent.com/ramsagarmeena/ShoonyaApi/main/NorenApi.py
!wget https://raw.githubusercontent.com/ramsagarmeena/ShoonyaApi/main/api_helper.py
```

##Login / Auth Flow



```
from api_helper import ShoonyaApiPy
api = ShoonyaApiPy()
#print("https://api.shoonya.com/OAuthlogin/investor-entry-level/login?api_key="+vc)
print(api.getOAuthURL(oauth_url="https://api.shoonya.com/OAuthlogin/authorize/oauth", api_key=vc))
```
Here vc is ClientID_U, pass as api_key -> Complete login on browser
it will redirect you with code to URL (you have given in API Key at trade.shoonya.com)
Put Redirect URL your own url, may be dummy url https://examplenamexxxxx.com like, because https://trade.shoonya.com/OAuthlogin/ will give error
copy that code and paste

```
code = input("Please enter code:")
api.getAccessToken(authcode=code, Secret_Code=secret_key, client_id=vc, UID=uid)

print(api.get_limits())
```

Here secret_key is the new key we got from trade.shoonya.com, vc is like F123456_U and uid is F123456

Rest of the Doc and functions are as follows 
https://pypi.org/project/norenrestapioauth/#description
