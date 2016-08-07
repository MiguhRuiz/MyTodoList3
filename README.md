# Cambios en Swift 3 en MyTodoList

Una colección de todos los cambios que vienen en Swift 3 y que afectan a la app MyTodoList creada en el [Curso de programación para iOS con Swift 2](https://platzi.com/cursos/programacion-apps-iphone-ipad-swift/) [de Platzi](https://platzi.com/)

> **[Recuerda que puedes acceder a este y a otros 79 cursos completamente gratis durante 1 mes usando mi enlace de referidos](https://platzi.com/r/MiguhRuiz)**

## Métodos afectados por orden alfabético

### `API.swift`

`UserDefaults.standard.object(forKey: "username")` **->** `NSUserDefaults.standardUserDefaults().objectForKey("username")`

`UserDefaults.standard.set(newUsername, forKey: "username")` **->** `NSUserDefaults.standardUserDefaults().setObject(newUsername, forKey: "username")`

`UUID().uuidString` **->** `NSUUID().UUIDString`

`return (uuid as NSString).substring(to: 5)` **->** `return (uuid as NSString).substringToIndex(5)`

`URLSession.shared` **->** `NSURLSession.sharedSession()`

`URL(string: "https://pendientesapp.herokuapp.com/todo")!` **->** `NSURL(string: "https://pendientesapp.herokuapp.com/todo")!`

`NSMutableURLRequest(url: url)` **->** `NSMutableURLRequest(URL: url)`

`request.httpMethod = "POST"` **->** `request.HTTPMethod = "POST"`

`DateFormatter()` **->** `NSDateFormatter()`

`dictionary["dueDate"] = formatter.string(from: date as Date)` **->** `dictionary["dueDate"] = formatter.stringFromDate(date)`

`dictionary["id"] = NSNumber(value: identifier)` **->** `dictionary["id"] = NSNumber(longLong: identifier)`

`JSONSerialization.data(withJSONObject: dictionary, options:  JSONSerialization.WritingOptions.prettyPrinted)` **->** `SJSONSerialization.dataWithJSONObject(dictionary, options:  NSJSONWritingOptions.PrettyPrinted)`

`String.Encoding.utf8.rawValue` **->** `NSUTF8StringEncoding`

`request.httpBody` **->** `request.HTTPBody`

`session.dataTask(with: request)` **->** `session.dataTaskWithRequest(request)`

`JSONSerialization.jsonObject(with: r, options: JSONSerialization.ReadingOptions.allowFragments)` **->** `NSJSONSerialization.JSONObjectWithData(r, options: NSJSONReadingOptions.AllowFragments)`

`DispatchQueue.main.async {responseBlock(err)}` **->** `dispatch_async(dispatch_get_main_queue()) {responseBlock(err)}`

### `AppDelegate.swift`

`UIUserNotificationSettings(types: [.alert, .badge], categories: nil)` **->** `UIUserNotificationSettings(forTypes: [.Alert, .Badge], categories: nil)`

`UIApplication.shared.registerUserNotificationSettings(settings)` **->** `UIApplication.sharedApplication().registerUserNotificationSettings(settings)`

`UIApplication.shared.registerForRemoteNotifications()` **->** `UIApplication.sharedApplication().registerForRemoteNotifications()`

` UIApplication.shared.applicationIconBadgeNumber = 0;` **->** `UIApplication.sharedApplication().applicationIconBadgeNumber = 0;`

`func application(_ application: UIApplication, didRegister notificationSettings: UIUserNotificationSettings)` **->** ` func application(application: UIApplication, didRegisterUserNotificationSettings notificationSettings: UIUserNotificationSettings)`
