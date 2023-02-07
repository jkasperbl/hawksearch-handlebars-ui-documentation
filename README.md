@bridgeline-digital/hawksearch-handlebars-ui / [Modules](modules.md)

# HawkSearch Handlebars UI

The HawkSearch Handlebars UI package allows you to add a highly-customizable search results page to your website powered by [HawkSearch](https://www.hawksearch.com/).

## Getting Started

1. Run `npm install --save @bridgeline-digital/hawksearch-handlebars-ui`
1. Modify your HTML by importing the HawkSearch Handlebars UI script file and adding the appropriate HTML elements.

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>HawkSearch Handlebars UI</title>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <script type="text/javascript">
      var HawkSearch = HawkSearch || {};

      HawkSearch.config = {
        clientId: "YOUR_CLIENTID_HERE"
      };
    </script>
    <script src="node_modules/@bridgeline-digital/hawksearch-handlebars-ui/dist/index.js" defer></script>
  </head>

  <body>
    <h1>HawkSearch Handlebars UI</h1>
    <hawksearch-search-field></hawksearch-search-field>
    <hawksearch-search-results></hawksearch-search-results>
  </body>
</html>
```

## Documentation

Please see the [documentation](https://hawksearch.atlassian.net/wiki/spaces/HUI) for this project.
