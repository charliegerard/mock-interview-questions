# Graceful Degradation vs. Progressive Enhancement

The most recent browsers can now support technologies like 3D graphics or innovative APIs like Web Bluetooth but not everyone updates their browsers to the latest versions, making the websites developers build sometimes inaccessible.
Graceful degradation and Progressive enhancement are two ways that attempt to solve this problem.

## Graceful degradation

This solution represents the practice of building a website or application that provide a good level of user experience in modern browsers, but will also degrade gracefully in older browsers.
Example with the use of CSS3 animations. If a specific transition is supported in Chrome but not IE, the element targeted will be animated in Chrome but will be static in IE.

## Progressive Enhancement

This technique is a bit similar but goes the opposite way. The website or application would be built to provide a base level of user experience for most browsers and would provide more advanced functionalities if the browser supports it.
