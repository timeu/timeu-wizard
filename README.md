[![Build Status](https://travis-ci.org/timeu/timeu-wizard.svg)](https://travis-ci.org/timeu/timeu-wizard)

_[Demo and API Docs](https://timeu.github.io/timeu-wizard/)_


## &lt;timeu-wizard&gt;


The `timeu-wizard` element displaying the progress of a wizard as a series of connected circles.  
By default the step number is displayed inside the circle and if provided a label below.  
The available steps are provided by either as an `array` of `Objects` or an `array` of `Strings`.

Simple example:


    
<!--
```
<custom-element-demo>
  <template>
      <script src="../webcomponentsjs/webcomponents-lite.js"></script>
      <link rel="import" href="timeu-wizard.html">
      <next-code-block></next-code-block>
  </template>    
</custom-element-demo>
```
-->
```html
<timeu-wizard steps='["Step1","Step2","Step3"]' step="2"></timeu-wizard>
```

By providing an `array` of `Objects` users can provide custom contents for the circles.

Example with custom circle content:
```html
<timeu-wizard steps='[{"label:Step1","content":"A"},{label:"Step2","content":"B"}]'></timeu-wizard>
```
It is also possible to display a vertical progress by adding the `vertical` attribute: 
```html
<timeu-wizard vertical steps='["Step1","Step2","Step3"]' step="2"></timeu-wizard> 
```
### Styling

The following custom properties and mixins are also available for styling:

Custom property | Description | Default
----------------|-------------|----------
`--timeu-wizard-line-color` | The color of the line  | `#dfdfdf`
`--timeu-wizard-line-size` | The thickness of the line | `1px`
`--timeu-wizard-circle-size` | The size of the circle | `40px`
`--timeu-wizard-filling-color` | The collor of the filling of the line | `#2db36f`
`--timeu-wizard-anim-speed` | The animation speed for the circles and lines | `0.5s`
`--timeu-wizard-active-color` | The color of finished steps and the current active step | `#2db36f`
`--timeu-wizard-label-font-size` | The font-size of the labels | `13px`
`--timeu-wizard-step-font-size` | The font-size of the steps inside of the circle | `25px`
`--timeu-wizard-circle-border-size` | The thickness of the circle border | `1px`
`--timeu-wizard` | Mixin applied to element host | {}
`--timeu-wizard-container` | Mixin applied to container div | {}
`--timeu-wizard-list` | Mixin applied to steps list | {}
`--timeu-wizard-list-item` | Mixin applied to each step | {}
`--timeu-wizard-list-item-active` | Mixin applied to each active step | {}
`--timeu-wizard-list-item-done` | Mixin applied to each done step | {}
`--timeu-wizard-list-item-icon` | Mixin applied to each step icon | {}
`--timeu-wizard-list-item-checkicon` | Mixin applied to each done step icon | {}
