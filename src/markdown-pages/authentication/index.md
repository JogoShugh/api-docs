Every request to the VersionOne API must have the Authorization HTTP Header set. You can do this using your username and password, but it is reccommended that you use an access token. Access tokens are associated with an application and grant the application certain access to resources. The application can act on behalf of the member who created the access token.

## Username and Password

You may use your username and password using Basic authentication by setting the Authorization header.
You'll have to base64 encode `username:password` including the `:` to accomplish this.

```bash
curl "https://V1Host/V1Instance/api_endpoint_here"
  -H "Authorization: Basic username:password"
```

## Access Tokens

VersionOne uses access tokens to grant access to the API. You can register a new access token by
logging into VersionOne and navigating to the Applications page. This is the suggested way to interact with the VersionOne API.

```bash
curl "https://V1Host/V1Instance/api_endpoint_here"
  -H "Authorization: Bearer <access-token>"
```


![Application Page](./../../images/access-token.png)

<aside class="notice">
  <div class="content">
    You can set your access token by clicking the avatar in the bottom left!
  </div>
</aside>