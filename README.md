# Disable-Screen-shot-in-Ios
This file disable screenshot in iOS devices 


You Must add This Funcation to Your App Delegate in ios Folder Like Example

```python
extension UIWindow {
func makeSecure() {
    let field = UITextField()
    field.isSecureTextEntry = true
    self.addSubview(field)
    field.centerYAnchor.constraint(equalTo: self.centerYAnchor).isActive = true
    field.centerXAnchor.constraint(equalTo: self.centerXAnchor).isActive = true
    self.layer.superlayer?.addSublayer(field.layer)
    field.layer.sublayers?.first?.addSublayer(self.layer)
  }
}
```
