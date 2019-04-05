# Optional-Value-Setter

It's easy wrapping to the optional value and it comes from [Swift Proposal: SE-0024](https://github.com/apple/swift-evolution/blob/master/proposals/0024-optional-value-setter.md)

### Soultion
```Swift
infix operator ??=

func ??=<T> (lhs: T?, defaultValue: T) -> T {
    
    guard let lhs = lhs else {
        return defaultValue
    }
    
    return lhs
}
```

### How to use it
```Swift
let text: String? = nil
let newText = (text ??= "Default new text") // Then the newText will eqaul "Default new text"

```

