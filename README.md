# Cambios en Swift 3 en MyTodoList

Una colección de todos los cambios que vienen en Swift 3 y que afectan a la app MyTodoList creada en el [Curso de programación para iOS con Swift 2](https://platzi.com/cursos/programacion-apps-iphone-ipad-swift/) [de Platzi](https://platzi.com/)

> **[Recuerda que puedes acceder a este y a otros 79 cursos completamente gratis durante 1 mes usando mi enlace de referidos](https://platzi.com/r/MiguhRuiz)**

## Métodos afectados por orden alfabético

### `API.swift`

`UserDefaults.standard.object(forKey: "username")` **->** `NSUserDefaults.standardUserDefaults().objectForKey("username")`
