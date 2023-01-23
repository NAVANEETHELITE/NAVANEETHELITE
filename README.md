
Document for releasing Xamarin.iOS app to testflight testing environment :

Step 1: Create a TestFlight Build

Open your Xamarin.iOS project in Visual Studio.

In the Solution Explorer, right-click on the project and select Properties.

In the Properties window, navigate to the iOS Bundle Signing tab.

Under the iOS Bundle Signing tab, select the "Automatically manage signing" option.

In the dropdown menu, select your development team and provisioning profile.

In the Solution Explorer, right-click on the project and select Archive.

Once the build is finished, the Organizer window will open. Select the archive and click the "Upload to App Store" button.

Step 2: Invite Users to Test

Open iTunes Connect and log in with your Apple ID.

In the top menu, select My Apps and select the app you want to test.

In the left sidebar, select TestFlight.

Under the Internal Testing tab, select the build you just uploaded and click the "Start Testing" button.

In the "Add testers" section, enter the email addresses of the users you want to invite to test the app.

Click the "Invite" button to send the invitations.

Step 3: Test the App

Users will receive an email with instructions on how to install the TestFlight app and download the beta version of your app.

Once the app is downloaded, users can start testing it and provide feedback through the TestFlight app.

As the developer, you can monitor the testing progress and receive feedback from the testers through the TestFlight section of iTunes Connect.
