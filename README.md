# Back-end
Google Calendar integration using OAuth2 mechanism in a Django REST API.

It provides two endpoints:
  /rest/v1/calendar/init/: This endpoint starts step 1 of the OAuth flow by prompting the user for their credentials.     
  /rest/v1/calendar/redirect/: This endpoint handles the redirect request sent by Google with the code for the token, gets the access token from the given code, and then   retrieves the list of events in the user's calendar.
The code uses the following APIs:
    google-auth-oauthlib.flow: This API is used to create an OAuth2 flow object and manage the OAuth2 authorization process.
    googleapiclient.discovery.build: This API is used to build a Google Calendar API service object to interact with the Google Calendar API.
    google.oauth2.credentials.Credentials: This API is used to manage OAuth2 credentials.
    google.auth.transport.requests: This API is used to manage HTTP requests for Google authentication.
