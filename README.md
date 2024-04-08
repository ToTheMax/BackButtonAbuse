# BackButtonAbuse

This is a Proof of Concept on how the browser back button can be abused to mislead a user.

## Use Case

- The user visits for example google.com and finds a link to our [page](https://tothemax.github.io/BackButtonAbuse/page.html)
- The user clicks on the link, gets sent to our website, but then presses the browsers back button
- The user thinks that he is back at google.com again, instead he is still on our (phishing?) page

## Fixes

The trick works for most browsers, only Chrome [fixed this](https://groups.google.com/a/chromium.org/g/blink-dev/c/T8d4_BRb2xQ/m/WSdOiOFcBAAJ) by requiring the user to first do a user interaction (i.e. a mouseclick). Therefore this script checks whether the page was accessed through a Chrome browser and then creates a fake cookie popup to make the user click.
**UPDATE: The trick works again on Chrome (except for the Android app)**

## Try it yourself

Visit the demo here 👉 [here](https://tothemax.github.io/BackButtonAbuse/page.html) 👈 and try to click the back button

## Resources

- https://groups.google.com/a/chromium.org/g/blink-dev/c/T8d4_BRb2xQ/m/WSdOiOFcBAAJ
- https://bugs.chromium.org/p/chromium/issues/detail?id=907167
- https://stackoverflow.com/questions/12381563/how-can-i-stop-the-browser-back-button-using-javascript
