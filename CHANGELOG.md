# Dimelo Android master #
 
## Dimelo Android 1.6.5 (December 4th, 2017) ##
- Fix: nullPointException when saving instance state (#31)
- Fix: refresh chat view on main thread

## Dimelo Android 1.6.4 (November 7th, 2017) ##
- Feature: add onOpen and onClose callback
- Feature: Support any kind of attachment for agent only
- Enhancement: Add the interactive push notification with direct reply
- Feature: Add new API to send a customer message

## Dimelo Android 1.6.3 (September 18th, 2017) ##
- Fix: Improve image quality (attachment + thumbnail)
- Fix: Add the JWT payload parsing in order to fill the attributes (mUserIdentifier, mUserName and mAuthenticationInfo)
- Fix: Add attachmentIcon customization option
- Fix: Remove scroll down animation when the message list is loaded for the first time

## Dimelo Android 1.6.2 (August 9th, 2017) ##
- Fix: check if camera permission is present in the manifest before display or hide the camera button
- Fix: prevent some push notifications to be lost if the SDK is not properly initialized (no userIdentifier)

## Dimelo Android 1.6.1 (July 25th, 2017) ##
- Fix: crash when displaying messages with attached photo

## Dimelo Android 1.6.0 (July 19th, 2017) ##
- Enhancement: add GIF support
- Fix: add camera files support for Android 7.0 (API 24) and above (#20)
- Fix: remove android:label in SDK manifest and app_name/sdk_name values in strings.xml

## Dimelo Android 1.5.3 (February 6th, 2017) ##
- Fix: nullPointException when stoping the app if attachments are disabled (#18)

## Dimelo Android 1.5.2 (January 31st, 2017) ##
- Fix: library attachment button was not clickable
- Enhancement: better handling of runtime permissions for attachment. Please don't forget to specify appropriate permissions in your AndroidManifest.
- Enhancement: check that camera device is available, otherwise disable camera attachment
- Fix: possible blinking effect of welcome message on multi-user installations

## Dimelo Android 1.5.1 (January 30th, 2017) ##
- Feature: Add feature asked in #17. You can now specify which activity should be launched when a notification has been clicked thanks to the new `consumeReceivedRemoteNotification` method:

```java
public static boolean consumeReceivedRemoteNotification(@NonNull Context context, @NonNull Bundle payload, @Nullable NotificationDisplayer notifDisplayer, @Nullable Class<?> activity);
```

## Dimelo Android 1.5.0 (January 18th, 2017) ##
- Feature: Add ability to disable attachments. It is now possible to disable the ability to send images and/or photos and/or location.
- Improvement: GMS is now an optional library. By default, the library is provided, but it can be excluded: the application will still work but location attachments will be disabled. Note that disabling location will not remove GMS from the dependencies.
- Fix: issue #13. Provide translation for the app_name provided in our strings.xml
- Fix: issue #14. Fix default color of the button in disable state
- Feature: related to issue #14. Add ability to customize the color of the send button is enabled state (see setSendButtonEnabledcolor)
- Fix: issue #15. setDeviceToken can now be run in a background thread without throwing exception.
- Fix: Rollback installationId fix of v1.4.2 and provide another instead. Now check the userIdenfier: notifications with a userIdentifier different from the current one will be skipped.

## Dimelo Android 1.4.4 (January 9th, 2017) ##
- Improvement: Reduce .aar size to ~320KB by removing dependency to RenderScript. Client apps do not need to include RenderScript anymore.

## Dimelo Android 1.4.3 (December 19th, 2016) ##
- Fix: Patch blinking effect of the welcome message at application startup.

## Dimelo Android 1.4.2 (December 9th, 2016) ##
- Change: Bump GMS dependency from v8.1.0 to v9.8.0.
- Fix: Check installationId when receiving a new notification. Only process notifications where the notificationId matches the current installationId.

## Dimelo Android 1.4.1 (November 28th, 2016) ##
- Fix: In the case no welcome message has been defined, the application was displaying a message containg the string "null". This is now fixed.

## Dimelo Android 1.4.0 (November 24th, 2016) ##
- Feature: Add ability to define a welcome message which is automatically displayed when a conversation is empty.
- Improvements: Some performance, security and accessibility improvements.

## Dimelo Android 1.3.1 (November 3rd, 2016) ##
- Fix: Do not strip whitespaces and newlines from JWT dictionary

## Dimelo Android 1.3.0 (October 19th, 2016) ##
- Feature: Add the UnreadCount feature to poll the number of unread messages.

## Dimelo Android 1.2.3 (October 11th, 2016) ##
- Feature: Allow customization of text size.

## Dimelo Android 1.2.2.2 (September 09th, 2016) ##
- Fix: Messages are now always correctly received and sent after internet recovery.
- Fix: Activity mode is now compatible with host applications that are not using AppCompat (Fixed crash when uploading an attachment)

## Dimelo Android 1.2.2.1 (August 25th, 2016) ##
- Fix: Messages are now correctly received and sent after internet recovery (when starting offline).

## Dimelo Android 1.2.2 (July 11th, 2016) ##
- Fix: Upgrade gradle to fix potential issues with native libraries.

## Dimelo Android 1.2.1 (July 5th, 2016) ##
- Fix: "Share" feature (removed hard-coded reference to autorithy `com.dimelo.fileprovider`).
- Fix: Use custom inherited FileProvider class to prevent conflicts.


## Dimelo Android 1.2.0 (May 19th, 2016) ##
- Feature: Remove local cache file
- Feature: Allow customization of attachments icon
- Fix: Compatibility with a wider range of Android Support libraries

## Dimelo Android 1.1.4 (May 19th, 2016) ##
- Fix: button geometry with Android API 19
- FIx: layout size calculation with Android Support Library > 23.3.0

## Dimelo Android 1.1.3 (May 11th, 2016) ##
- Fix: compatibility with Android Support Library > 23.1

## Dimelo Android 1.1.2 (April 14th, 2016) ##
- Feature: It is now possible to customize text message and attachments background with different bubbles
- Feature: It is now possible to customize the color the send message arrow when disabled (no text & no attachment selected)
- Fix: Fixed crash which occured when the SDK was used without `com.google.android.geo.API_KEY`

## Dimelo Android 1.1.1 (January 13th, 2016) ##
- Fix: Fixed crash when calling setUserIdentifier or setJwt after first chat setup.

## Dimelo Android 1.1.0 (December 18th, 2015) ##
- Feature: Added support for image and location attachments.


## Dimelo Android 1.0.0 (July 7th, 2015) ##
- Feature: First official release supporting Dimelo Mobile protocol but limited to text
  interaction.
