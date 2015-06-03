##  W3C - Web Components

http://www.w3.org/TR/2013/WD-components-intro-20130606/

Custom elements can encapsulate state and provide script interfaces.

```html
<element extends="button" name="fancy-button">
  ...
</element>

<element name="tick-tock-clock">
 <script>
    ({
      tick: function () {
      }
    });
 </ script>
</element>
```
