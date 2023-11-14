## Speedgeeking at European DevSummit Berlin 2023: 
# Four types of widget communication in ArcGIS Experience Builder

## WidgetManager
### Controlling the widget state

You can control the state of a widget on the UI by using the WidgetManager. In the official samples repo, you can find a sample showing this approach.

It's called ['Control the widget state'](https://github.com/Esri/arcgis-experience-builder-sdk-resources/tree/master/widgets/control-the-widget-state). It identifies 
* sidebar widgets in your app and 
* widgets living inside a controller widget
and toggles if they appear expanded or collapsed.

![](./assets/control-widget-state.gif)

### The crucial point

Use an ``appAction`` imported from the jimu framework to dispatch a ``openWidget`` or ``closeWidget`` action along with the widgetId via the global AppStore.

Like here: 
https://github.com/Esri/arcgis-experience-builder-sdk-resources/blob/master/widgets/control-the-widget-state/src/runtime/widget.tsx#L103