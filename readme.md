# Web Monetization

Web Monetization is a browser API which allows a website to make money without using ads and without requiring any user interaction. The user signs up to a Web Monetization Provider like Coil, and the provider sends micropayments to Web Monetized websites whenever the user visits them.

# Exclusive Content (Basic)

One of the perks of Web Monetization is that its JavaScript API can be used to make your page respond to Web Monetization. 
You can reward the people who support your site by giving web monetized viewers exclusive content.

This is a basic example of showing exclusive content only to web monetized visitors.

### ← index.html

The `monetization` meta tag contains a payment pointer, which is the digital wallet address to send micropayments to.

To see the "View as Web Monetized visitor" button, you **must** view the page in an iframe, not in a new window.

### ← exclusive-content-basic.js

Listens for the `monetizationstart` event, then makes the exclusive content element visible by removing the defined CSS class.

### ← wm-previewer.js

Simulates Web Monetization and adds the "View as Web Monetized visitor" button to `index.html`. This script only activates in iframe.

### ← css/exclusive-content.css

Contains the class used to hide exclusive content. The `exclusive-content-basic.js` removes the class for web monetized visitors, making the content visible.

# Additional References

If you're viewing this outside of webmonetization.org, you can find more information here:

* [Webmonetization.org](https://webmonetization.org)
* [Exclusive Content doc on webmonetization.org](https://webmonetization.org/docs/exclusive-content)