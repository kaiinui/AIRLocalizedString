AIRLocalizedString
==================

`AIRLocalizedString` allows you to update i18n texts without compelling users to update the App.

```objc
[AIRLocalizedString setRemoteBaseURL:@"https://s3.amazonaws.com/.../"];

AIRLocalizedString(@"Hello World!", @"");

// => "こんにちは！"
```

And place `.strings` file for each languages you support as follows.

```
Base URL
|
|- en.strings
|- fr.strings
|- it.strings
...
```

`AIRLocalizedString()` fallbacks to default `NSLocalizedString()` if it has not retrieved latest i18n from remote URL (typically on first run), or if there is no `.strings` on the remote.
