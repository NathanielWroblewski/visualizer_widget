Dashing Visualization Widget
=
Description
-

A [Dashing](http://shopify.github.com/dashing) widget to display visualizations for any audio your microphone can detect.  This widget uses the totally awesome [APEXvj](http://www.apexvj.com/) for basically everything.

Preview
-
![Screen Shot](http://i.imgur.com/eDqMSzK.png)
![Screen Shot](http://i.imgur.com/bCtbjVm.png)
![Screen Shot](http://i.imgur.com/rv3a7Gi.png)
![Screen Shot](http://i.imgur.com/Jha839K.png)
![Screen Shot](http://i.imgur.com/32M62u2.png)

Useage
-
To use this widget, copy `visualizer.coffee`, `visualizer.html`, and `visualizer.scss` into the `/widgets/visualizer` directory of your Dashing app. This directory does not exist in new Dashing apps, so you may have to create it.

To include the widget in a dashboard, add the following to your dashboard layout file:

#####dashboards/sample.erb

```HTML+ERB
...
  <li data-row="1" data-col="1" data-sizex="2" data-sizey="1">
    <div class="visualize" data-id="visualizer" data-view="Visualizer"></div>
  </li>
...
```

Code
-
#####widgets/visualizer/visualizer.coffee

```coffee

class Dashing.Visualizer extends Dashing.Widget

```

#####widgets/visualizer/visualizer.html

```HTML
<iframe src="http://www.apexvj.com/kaksi/webgl8/index.html?i=1" width="610" height="360" style="-webkit-transform:scale(1.0);-moz-transform-scale(1.0);" frameBorder="0">
</iframe>
```

#####widgets/visualizer/visualizer.scss

```SCSS
$background-color:  black;

.visualize {
  padding: 0px;
}
.visualizer {
  padding: 0px;
  margin: 0px;
  background-color: $background-color;
  iframe {
    width: 100%;
    height: 100%;
  }
}
```
