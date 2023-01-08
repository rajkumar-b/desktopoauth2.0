# Flutter Desktop App OAuth2.0 with PKCE

A flutter plugin for Desktop app OAuth2.0 protocol (Authorization Code ) by using a desktop browser. From the desktop App, the plugin delegates the authentication flow to a desktop browser. After successful authentication, this plugin fetches the authorization code from the browser and then fetches the access token from the authorization server.    

## Features

1. Authorization Code Flow
2. PKCE enabled
3. Client Secrect support

## Getting started

TODO: List prerequisites and provide or point to information on how to
start using the package.

## Add dependency

```yaml
dependencies:
  desktopoauth2: lastest version  
```


## Usage


```dart
                    DesktopAuthorizationCodeFlow desktopAuthCodeFlow = DesktopAuthorizationCodeFlow();

                    //state //Optional
                    desktopAuthCodeFlow.authState = '';
                     //Authorize Access URL
                    desktopAuthCodeFlow.authorizationUrl = '';
                    // Client id
                    desktopAuthCodeFlow.clientId = '';
                    // Any port
                    desktopAuthCodeFlow.localPort = 9298;
                     //PKCE or Client Secret
                    desktopAuthCodeFlow.pkce = true;
                    //Redirect URI example - http://localhost:9298/callback
                    desktopAuthCodeFlow.redirectUri = '';
                    //Scope
                    desktopAuthCodeFlow.scopes = ['openid'];
                    //Token Access URL
                    desktopAuthCodeFlow.tokenUrl = '';

                    desktopOAuth2.oauthorizeCode(desktopAuthCodeFlow).then((token) {
                      if (token != null && token.isNotEmpty) {
                        accessToken = token["access_token"];
                      }
                    });
```#   d e s k t o p o a u t h 2 . 0  
 #   d e s k t o p o a u t h 2 . 0  
 