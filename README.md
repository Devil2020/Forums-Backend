# ForumsBackend
#### a fake json for implementing a backend driven form

### Keybord Type
```swift
enum KeyboardType: Int {
  case default = 0
  case email = 1
  case number = 2
  case phone = 3
}
```

### Message 
```swift
struct Message {
  let error: String
  let empty: String
}
```

##### Colors in Hex format, ex: "#ffe700ff" 
##### Validation in Regex format, ex: "[A-Z0-9a-z._%+-]+@[A-Za-z0-9.-]+\\.[A-Za-z]{2,64}"

### Style
```swift
struct Style {
  let textColor: String
  let accentColor: String
  let placeholderColor: String
  let borderColor: String
  let backgroundColor: String
  let cornerRadius: Double
}
```

### TextField
```swift
struct TextField {
  let id: Int
  let matchingId: Int?
  let placeholder: String
  let type: KeyboardType
  let isSecured: Bool
  let style: Style
  let validation: String
  let message: Message
}
```

### Response
```swift
struct Response {
  let count: Int
  let fields: [TextField]
}
```
