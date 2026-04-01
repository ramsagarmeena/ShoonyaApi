# ShoonyaApi
# Shoonya Python Api
##Login / Auth Flow

```
from api_helper import ShoonyaApiPy
api = ShoonyaApiPy()
#print("https://api.shoonya.com/OAuthlogin/investor-entry-level/login?api_key="+vc)
print(api.getOAuthURL(oauth_url="https://api.shoonya.com/OAuthlogin/authorize/oauth", api_key=vc))
```
Here vc is ClientID_U, pass as api_key -> Complete login on browser
it will redirect you with code to URL (you have given in API Key at trade.shoonya.com)
Put Redirect URL your own url, may be fake url, because https://trade.shoonya.com/OAuthlogin/ will give error
copy that code and paste

```
code = input("Please enter code:")
api.getAccessToken(authcode=code, Secret_Code=secret_key, client_id=vc, UID=client_id)

print(api.get_limits())
```

Here secret_key is from trade.shoonya.com

Rest of the Doc and functions are as follows 
https://pypi.org/project/norenrestapioauth/#description
