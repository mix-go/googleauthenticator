> OpenMix 出品：[https://openmix.org](https://openmix.org/mix-go)

## Mix Google Authenticator

Generate Secret

```go
secret := googleauthenticator.GenerateSecret()
```

Generate Code

```go
code := googleauthenticator.GenerateToken()
```

Verify Code

```go
ok := googleauthenticator.VerifyToken(secret, code)
// or
ok := googleauthenticator.VerifyTokenCustom(secret, code, 60)
```

Generate Url

```go
uri := googleauthenticator.GenerateTotpUri("Foo", "bar", secret)
// or
url := googleauthenticator.GenerateQRCodeGoogleUrl("Foo", "bar", secret)
```

## License

Apache License Version 2.0, http://www.apache.org/licenses/