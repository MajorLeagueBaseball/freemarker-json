# Freemarker JSON Macro

This macro takes a Freemarker model and prints it out as JSON. Output is compressed to a single line.

## Usage

```
<#import "json.ftl" as json>

<@json.stringify your_model_here />
```

## Escaping

Escape the generated JSON with the second argument to `<@json.stringify>`. The options are `html` and `js_string`.

```html
<meta name="extraData" content='<@json.stringify extra_data "html" />' />

<script type="text/javascript">

var myExtraJSON = '<@json.stringify extra_data "js_string" />';

// of course, if you need the data, not a JSON string, you can do this:
var myExtraData = <@json.stringify extra_data />;

</script>
```
