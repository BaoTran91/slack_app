# slack_app
testing slack api


https://api.slack.com/tutorials/slack-apps-and-postman

1. Create a Slack App
Create a Slack App by navigating directly to the Create App page. Fill out all the required fields.

Creating your app

2. Get Client ID and Secret for later
On the Basic Information page, scroll down and note the Client ID and Client Secret. For this tutorial, we will copy this information into Postman.

3. Add the Postman OAuth Callback URL to your Redirect URLs.
On the left navigation, click OAuth & Permissions. Here, add the following URL to your list of Redirect URLs: https://www.getpostman.com/oauth2/callback.

Redirect URLs

If you are looking specifically to get a Grid-level scope, like admin or auditlogs:read, you will need to also make your app publicly distributed. More on this here.

4. Navigate to Postman's Authorization Menu
Now that we have a Slack App to authorize against, we will setup an OAuth 2.0 client. In Postman's Authorization menu, select OAuth 2.0 for the type.

Postman configuration

⚠️ Note: You may need to remove Cookies if you already have a session saved in Postman. ⚠️

Postman Cookies

5. Click the Get New Access Token Button
Once OAuth 2.0 is selected as the type, click the Get New Access Token button to open the OAuth configuration modal.

Get that access token

6. Configure the OAuth settings
Here we will setup the OAuth client. We'll pull information from multiple sources to complete this form:

Callback URL https://www.getpostman.com/oauth2/callback
Auth URL: https://slack.com/oauth/authorize
Access Token URL: https://slack.com/api/oauth.access
Client ID: Copy the Client ID value from step 2
Client Secret: Copy the Client Secret value from step 2
Scope: A space-separated list of OAuth scopes. A complete list of scopes are here.
Client Authentication: Send client credentials in the body
🤖 For bot tokens, the following parameters will use v2:

Auth URL: https://slack.com/oauth/v2/authorize
Access Token URL: https://slack.com/api/oauth.v2.access
Scopes

7. Press the Request Token button
If you set everything up correctly and pressed Request Token, you should see a familiar Slack authorization window. Select the team you would like to authorize and validate your scopes match what's presented.

Authorization

