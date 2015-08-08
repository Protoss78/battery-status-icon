# battery-status-icon
A web component that detects and displays the current battery status as an icon. It uses Polymer 1.x and in case a browser still supports the currently deprecated HTML5 battery API it also auto detects the battery status. But the battery level and charging status can also be set from the outside (e.g. in combination with Cordova and the battery plugin).

Example:

```html
<paper-material>
    <h1>No Label</h1>
    <battery-status-icon></battery-status-icon>
    <battery-status-icon level="33" charging></battery-status-icon>
    <battery-status-icon level="15"></battery-status-icon>
    <battery-status-icon level="66"></battery-status-icon>
</paper-material>
<paper-material>
    <h1>With Label</h1>
    <battery-status-icon></battery-status-icon>
    <battery-status-icon level="33" charging show-label></battery-status-icon>
    <battery-status-icon level="15" show-label></battery-status-icon>
    <battery-status-icon level="66" show-label></battery-status-icon>
</paper-material>
```
