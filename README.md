# battery-status-icon
A web component that autodetects and displays the current battery status as an icon. It uses Polymer 1.x and the new HTML5 Navigator.getBattery() API. Alternatively the battery level and charging status can also be set from the outside (e.g. in combination with Cordova and the battery plugin).

Install:
```
bower i battery-status-icon -S
```
### Docs and Demo
[Can be found here.](http://protoss78.github.io/battery-status-icon/components/battery-status-icon/)

### Example:

```html
<battery-status-icon></battery-status-icon>
<battery-status-icon level="33" charging></battery-status-icon>
<battery-status-icon level="15" show-label></battery-status-icon>
<battery-status-icon level="66" color-levels></battery-status-icon>
<battery-status-icon autodetect show-label color-levels></battery-status-icon>
```

![Preview](https://raw.githubusercontent.com/Protoss78/battery-status-icon/master/preview.png)

### Styling
    
The following custom properties are available for styling:
  
Custom property | Description | Default
----------------|-------------|----------
`--battery-icon-size` | Size of battery icon displayed. | `24px`
`--battery-default-color` | Color of battery when colorLevels is false. | `#323`
`--battery-high-color` | Color of battery when above 80%. | `Green`
`--battery-mid-color` | Color of battery when between 80% >< 20%. | `Orange`
`--battery-low-color` | Color battery when below 20%. | `Red`
