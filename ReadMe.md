# README

Authenticated endpoints


## Get the access token

### This will give you an access token you can use for hitting any of the endpoints that are private in this API.

YOUR_CLIENT_SECRET=XHCyn5L1XF7oT4oQVs1aHNQcieshII_r1Er4p9PaQNOjJ56Oxm-Gxw0QGrXAOz7A
YOUR_API_IDENTIFIER=https://quickstarts/api


curl -i --request POST \
  --url 'https://paddington.eu.auth0.com/oauth/token' \
  --header 'content-type: application/json' \
  --data '{"grant_type":"client_credentials","client_id": "U7TZy4Jgg3_uzhAv4r5eg20gN0alo-dg","client_secret": "YOUR_CLIENT_SECRET","audience": "YOUR_API_IDENTIFIER"}'


## hit the endpoint using that token

curl -i --request GET \
  --url http://localhost:3010/api/private \
  --header 'authorization: Bearer YOUR_ACCESS_TOKEN'