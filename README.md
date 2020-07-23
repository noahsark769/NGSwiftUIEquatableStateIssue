# NGSwiftUIEquatableStateIssue
The following SwiftUI code causes an app crash on launch, with the Xcode 12 AppKit App Delegate app template.

```swift
struct NormalExperienceState {
    var one: String?
    var two: String?
    var three: String?
    var four: String?
    var five: String?
    var six: String?
    var seven: String?
    var eight: String?
    var nine: String?
    var ten: String?
    var eleven: String?
    var twelve: String?
    var thirteen: String?
}

struct ContentView: View {
    @State var state = NormalExperienceState()
    var body: some View {
        Text("Hello, world!").padding()
    }
}
```

Steps to reproduce:

1. Clone the git repository at https://github.com/noahsark769/NGSwiftUIEquatableStateIssue
2. Open the xcworkspace in Xcode, run the app (tested on a Macbook Pro with OSX 10.15.5)

Expected: The app runs
Actual: The app crashes

Note: You may need to add another var to the NormalExperienceState struct, I've seen it behave inconsistently across compiles.

Note: The same issue doesn't seem to happen on iOS with the same content view.
