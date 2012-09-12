## Status Bar Style

Available styles:

* `UIStatusBarStyleDefault`
* `UIStatusBarStyleBlackTranslucent`
* `UIStatusBarStyleBlackOpaque`

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

## Status Bar Visibility

Available animations:

* `UIStatusBarAnimationNone`
* `UIStatusBarAnimationFade`
* `UIStatusBarAnimationSlide`

### Example

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    application.setStatusBarHidden(true, withAnimation:UIStatusBarAnimationSlide)
    # …    
    true
  end
end
```