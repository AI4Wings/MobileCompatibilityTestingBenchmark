Category: Category

Type:

- New features and APIs: New features introduced in Android 15.
- Change (all apps): Constraints that all versions of the app must comply with.
- Change (apps targeting 15+): Constraints that apply to apps targeting Android 15 and higher as the platform.

Name: Description

Info:Specific Detailed Description

Describe: Detailed Description

API_List: Relevant code APIs, XML attributes, etc.

Source: If manually added, the field should be marked as "Manually Added." If sourced from the internet, include the corresponding link.

Example:

```
Category, Type, Name, Info, Describe, API_List, Source
"Security","Change (apps targeting 15+)","Secured background activity launches","For apps targeting Android 15, we've included further changes to prevent malicious background apps from bringing other apps to the foreground, elevating their privileges, and abusing user interaction.","Android 15 protects users from malicious apps and gives them more control over their devices by adding changes that prevent malicious background apps from bringing other apps to the foreground, elevating their privileges, and abusing user interaction. Background activity launches have been restricted since Android 10 (API level 29).\n\nOther changes\nIn addition to the restriction for UID matching, these other changes are also included:\n\nChange PendingIntent creators to block background activity launches by default. This helps prevent apps from accidentally creating a PendingIntent that could be abused by malicious actors.\nDon't bring an app to the foreground unless the PendingIntent sender allows it. This change aims to prevent malicious apps from abusing the ability to start activities in the background. By default, apps are not allowed to bring the task stack to the foreground unless the creator allows background activity launch privileges or the sender has background activity launch privileges.\nControl how the top activity of a task stack can finish its task. If the top activity finishes a task, Android will go back to whichever task was last active. Moreover, if a non-top activity finishes its task, Android will go back to the home screen; it won't block the finish of this non-top activity.\nPrevent launching arbitrary activities from other apps into your own task. This change prevents malicious apps from phishing users by creating activities that appear to be from other apps.\nBlock non-visible windows from being considered for background activity launches. This helps prevent malicious apps from abusing background activity launches to display unwanted or malicious content to users.","['allowCrossUidActivitySwitchFromBelow', 'PendingIntent', 'activity']","https://developer.android.com/about/versions/15/behavior-changes-15#secured-bal"
```
