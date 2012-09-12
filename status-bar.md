## Status Bar Style

Available styles:

* UIStatusBarStyleDefault,
* UIStatusBarStyleBlackTranslucent,
* UIStatusBarStyleBlackOpaque

### Example

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    application.setStatusBarStyle(UIStatusBarStyleBlackOpaque, animated:true)
    # …
    true
  end
end
```