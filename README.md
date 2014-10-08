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
|- ja.strings
...
```

Content of `.strings` is as you are familiar with.

```
"Hello World!" = "こんにちは！";
```

`AIRLocalizedString()` fallbacks to default `NSLocalizedString()` if it has not retrieved latest i18n from remote URL. (typically on first run), or if there is no `.strings` on the remote.

Author
---

kaiinui (lied.der.optik@gmail.com)

LICENSE
---

```
The MIT License (MIT)

Copyright (c) 2014 kaiinui

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
