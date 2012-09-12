## Example

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    @window = UIWindow.alloc.initWithFrame(UIScreen.mainScreen.bounds)
    @window.rootViewController = UIViewController.alloc.init
    @window.makeKeyAndVisible()
    
    notification = UILocalNotification.alloc.init
    notification.fireDate = NSDate.dateWithTimeIntervalSinceNow(10)
    notification.alertBody = "My first notification"
    notification.alertAction = "Yo."
    notification.applicationIconBadgeNumber = 1
    application.scheduleLocalNotification(notification)
    
    true
  end
end
```

## Links

* [iOS Developer Library: Scheduling, Registering, and Handling Notifications](http://developer.apple.com/library/ios/#documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/IPhoneOSClientImp/IPhoneOSClientImp.html#//apple_ref/doc/uid/TP40008194-CH103-SW1)