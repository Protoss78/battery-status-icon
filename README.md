[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/Protoss78/battery-status-icon)

# battery-status-icon
A web component that autodetects and displays the current battery status as an icon. It uses Polymer 1.x and the new HTML5 Navigator.getBattery() API. Alternatively the battery level and charging status can also be set from the outside (e.g. in combination with Cordova and the battery plugin).

Install:
```
bower i battery-status-icon -S
```

### Example:

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="battery-status-icon.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
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
  `--battery-icon-rotate` | Use rotate(x) to rotate the battery icon.<br>Sample: --battery-icon-rotate: rotate(270deg); | `rotate(0deg)`
  
  __Style example:__
  
<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="battery-status-icon.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<style>
    .changing-example {
        --battery-low-color: #D32F2F;
        --battery-mid-color: #F57C00;
        --battery-high-color: #388E3C;
        --battery-icon-size: 48px;
        --battery-label-background: #455A64;
        --battery-label-opacity: 1;
        --battery-label-text-color: #CFD8DC;
    }
    /* Battery Icon is rotated by 270° (left to right) */
    .left-to-right {
      --battery-icon-rotate: rotate(270deg);
    }
    
    /* Battery Icon is rotated by 90° (right to left) */
    .right-to-left {
      --battery-icon-rotate: rotate(90deg);
    }
</style>
<battery-status-icon label-position="bottom" class="changing-example" level="0" color-levels
                     charging show-label></battery-status-icon>                               
<battery-status-icon class="left-to-right" autodetect show-label color-levels></battery-status-icon>
<battery-status-icon class="right-to-left" autodetect show-label color-levels></battery-status-icon>
```  
