# Freemarker JSON Macro

This macro takes a Freemarker model and prints it out as JSON. Output is compressed to a single line.

## Usage

```html
<#import "json.ftl" as json>

<@json.stringify your_model_here />
```

## Options

You can pass a second argument to `<@json.stringify>` if you want the JSON escaped. The options are `"html"` and `"js_string"`.

```html
<meta name="extraData" content='<@json.stringify extra_data "html" />' />

<script type="javascript">

var myExtraJSON = '<@json.stringify extra_data "js_string" />';

// of course, if you need the data, not a JSON string, you can do this:
var myExtraData = <@json.stringify extra_data />;

</script>
```
