---
layout: post
title: Swift-Wkwebkits
categories:
- swift
---

When we are trying to write some swift apps including OSX and IOS basic on webkit that apple provides, the question will be how can I receive a call-back from js. **WKwebkit** can help us to solve the problem. It provides the protocol  called `WKScriptMessageHandler: Provides a method for receiving messages from JavaScript running in a webpage.` This is enough talking lets see some example.


{% highlight swift %}
class NotificationScriptMessageHandler: NSObject, WKScriptMessageHandler {
    func userContentController(userContentController: WKUserContentController, didReceiveScriptMessage message: WKScriptMessage!) {
        print(message.body)
    }
}
{% endhighlight %}

Provides the method of using WKScriptMessage protocols.
