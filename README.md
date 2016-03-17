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
<battery-status-icon level="50" show-label label-position="top"></battery-status-icon>
<battery-status-icon level="66" color-levels></battery-status-icon>
<battery-status-icon autodetect show-label color-levels></battery-status-icon>
```

__Attributes:__

Attribute | Description | Default
  ----------------|-------------|----------
  `autodetect` | Auto detect battery level, rather than static input | `false`
  `charging` | Detects if device is charging (Can be set manually) | `false`
  `color-levels` | Change color depending on remaining battery level | `false`
  `label-position` | Where the label should render (top, right, bottom, left) | `right`
  `level` | Container for battery level value(Can be set manually) | `NULL`
  `show-label` | Shows label on mouse over if true. | `false`

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
  `--battery-label-background` | Background color of tooltip label. | `#616161`
  `--battery-label-opacity` | Opacity level of tooltip label. | `0.9`
  `--battery-label-text-color` | Text color of tooltip label | `White`
  
  __Style example:__
  
  This part of the code needs to be within your head tags, or imported as part of your app-theme.html
  
  ```html
  <style is="custom-style">
    :root {
      --battery-default-color: #455A64;
      --battery-low-color: #D32F2F;
      --battery-mid-color: #F57C00;
      --battery-high-color: #388E3C;
      --battery-icon-size: 48px;
      --battery-label-background: #455A64;
      --battery-label-opacity: 1;
      --battery-label-text-color: #CFD8DC;
    }
  </style>
```
