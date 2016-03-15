# battery-status-icon
A web component that autodetects and displays the current battery status as an icon. It uses Polymer 1.x and the new HTML5 Navigator.getBattery() API. Alternatively the battery level and charging status can also be set from the outside (e.g. in combination with Cordova and the battery plugin).

Install:
```
bower i battery-status-icon -S
```

Example:

```html
<paper-material>
    <h1>No Label</h1>
    <battery-status-icon></battery-status-icon>
    <battery-status-icon level="33" charging></battery-status-icon>
    <battery-status-icon level="15" show-label></battery-status-icon>
    <battery-status-icon level="66"></battery-status-icon>
    <battery-status-icon autodetect show-label></battery-status-icon>
</paper-material>
```
![Preview](https://github.com/Protoss78/battery-status-icon/raw/master/preview.png)
