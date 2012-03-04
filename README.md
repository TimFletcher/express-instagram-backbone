Express is a simple image gallery using the Instagram API and backbone.js. It
authenticates itself with your Instagram account using OAuth 2 and stores the
access token in HTML5 local storage. This is entirely a javascript app. There
is no server side component whatsoever.

## Developer Account Setup

Instagram requires that, for API access to user data, you register your
application. You can do this by creating an account at `http://instagr.am/developer/register/`

## Adding a Client

You need to register a client app in your developer account. You can put pretty
much anything in for most of the fields but make sure that your callback url is
`http://localhost:8000`

## Running the App

You need to enter your client ID into the app code. Change `*** YOUR CLIENT ID
***` as appropriate.

I'm on OS X and you can easily run a quick web server using Python. There's no
server side component to Express so you just need to `cd` into the root of the
project and run the following:

    python -m SimpleHTTPServer

## Caveats

This is a pretty simple but functional proof of concept. The main issue is that
the OAuth access token is not persisted server side so if you clean out your
browser you'll lose access with that particular token. You can reauthenticate
and get a new token, of course.

## ToDo

I'd like to use `http://parse.com` to persist access tokens and maybe provide
some kind of simple gallery hosting where users could quickly register and see
their Instagram galleries.
