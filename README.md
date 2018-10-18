# LoginSample
This is a sample project to replicate bug https://developers.facebook.com/support/bugs/311398809643074/?disable_redirect=0

SSO logs in fine whenever the user has the Facebook App installed, and ask the user to sign in through the native app.
The issue is when the user doesn't have the app installed and asks to user to log into facebook through the browser

System specs
Android
lib: 'com.facebook.android:facebook-android-sdk:4.37.0'
Application: NP Dodge Real Estate (You can find on playstore)

I've labeled the steps on the screenshots for reproduction purposes
1. In order to reproduce you will need to disable or delete the Facebook app from your phone
2. Click the Sign In with Facebook button. User is redirected to facebook log-in as shown in screenshot (SSO_step1)
3. Log in. User is redirected to 'Confirm Login' screen (SSO_step3)
4. Once user clicks the continue button, user is redirected back to facebook log-in (SSO_step4)
5. Try logging in again.  User is then redirected to screen where facebook is Loading infinitely (SSO_step6)

I would expect SSO to return the auth key after the user clicks the 'Continue' button on the 'Confirm Login' screen
