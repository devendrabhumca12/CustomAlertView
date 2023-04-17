# CustomAlertView

CustomAlertView is a customizable and reusable alert view for SwiftUI applications. It allows you to easily display alerts with custom titles, messages, buttons, and images.

## Features
- Customizable title, message, and buttons
- Option to add an image to the alert
- Easy to integrate with SwiftUI apps
- Fully customizable styling
- Support for primary and secondary buttons

## Requirements
- iOS 13.0+ / macOS 10.0+ / tvOS 13.0+ / watchOS 6.0+
- Xcode 12.0+
- Swift 5.3+

## Installation

### Manual
1. Download and unzip the source code.
2. Drag and drop the **"CustomAlertView.swift"** file into your Xcode project
3. Make sure that "Copy items if needed" and your project target are selected
4. Click "Finish" to complete the installation

## Usage

```swift
1. Add a `CustomAlertView` instance to your view hierarchy:
CustomAlertView(
    title: "Success!",
    message: "Your profile was updated successfully.",
    primaryButtonLabel: "OK",
    primaryButtonAction: {}
)

2. Customize the alert view by providing additional parameters:
CustomAlertView(
    title: "Error!",
    message: "There was an error updating your profile.",
    primaryButtonLabel: "Try Again",
    primaryButtonAction: {},
    secondaryButtonLabel: "Cancel",
    secondaryButtonAction: {}
)

3. Present the alert view when necessary, for example, in response to a button tap event:
Button("Show Alert") {
    self.showAlert = true
}
.alert(isPresented: self.$showAlert) {
    CustomAlertView(
        title: "Success!",
        message: "Your profile was updated successfully.",
        primaryButtonLabel: "OK",
        primaryButtonAction: {}
    )
}
```

## Customization
The CustomAlertView can be customized in various ways:

1. **Title** : A string that represents the alert view's title. If nil, the image parameter will be used instead.
2. **Message**: A string that represents the alert view's message.
3. **Primary button label**: A string that represents the primary button's label text.
4. **Primary button action**: A closure that represents the primary button's action.
5. **Secondary button label**: An optional string that represents the secondary button's label text.
6. **Secondary button action**: An optional closure that represents the secondary button's action.
7. **Image**: An optional Image instance that represents the alert view's image.
8. **font**: The font to use for the title and message
9. **titleColor**: The color to use for the title text
10. **messageColor**: The color to use for the message text
11. **primaryButtonColor**: The color to use for the primary button background
12. **primaryButtonTextColor**: The color to use for the primary button text
13. **secondaryButtonColor**: The color to use for the secondary button background
14. **secondaryButtonTextColor**: The color to use for the secondary button text
15. **blurStyle**: The style of the background blur effect

## Examples
The following examples demonstrate how to use the CustomAlertView in different scenarios:

```swift
CustomAlertView(
    title: "Success!",
    message: "Your profile was updated successfully.",
    primaryButtonLabel: "OK",
    primaryButtonAction: {}
)

CustomAlertView(
    title: "Error!",
    message: "There was an error updating your profile.",
    primaryButtonLabel: "Try Again",
    primaryButtonAction: {},
    secondaryButtonLabel: "Cancel",
    secondaryButtonAction: {}
)

CustomAlertView(
    title: "Confirmation",
    message: "Are you sure you want to delete this item?",
    primaryButtonLabel: "Yes",
    primaryButtonAction: {},
    secondaryButtonLabel: "No",
    secondaryButtonAction: {}
)

CustomAlertView(
    title: "Warning!",
    message: "You are about to perform a critical operation.",
    primaryButtonLabel: "Proceed",
    primaryButtonAction: {},
    secondaryButtonLabel: "Cancel",
    secondaryButtonAction: {}
)

CustomAlertView(
    message: "An error occurred.",
    primaryButtonLabel: "OK",
    primaryButtonAction: {},
    secondaryButtonLabel: nil,
    secondaryButtonAction: nil,
    image: Image(systemName: "exclamationmark.triangle")
)
```

or Check out the CustomAlertView_Previews file for examples of how to use CustomAlertView in your SwiftUI app.
            
## Contact
If you have any questions or feedback, feel free to contact me at **devendra.bhumca12@gmail.com**.
