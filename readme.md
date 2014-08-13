# Polymer Anchor Query

## Installation

```
bower install reggi/polymer-anchor-query --save
```

## Usage

Drop the following lines within the `<head>` tag.

  <script src="./bower_components/platform/platform.js"></script>
  <link rel="import" href="./bower_components/polymer-anchor-query/anchor-query.html">

To create a new banner use the `<anchor-query>` tag.

### Usage Option 1

You can pass in any custom attribute to the `<anchor-query>` tag itself and it will urlencode it and append it to the `href`.

```
<anchor-query href="https://twitter.com/share" text="This tweet was sent via <anchor-query>!" via="thomasreggi" hashtags="polymer,webcomponent,html" url="https://github.com/reggi/polymer-anchor-query">
  <i class="fa fa-twitter"></i>
</anchor-query>

```

### Usage Option 2

You can nest the `<query-param>` within `<anchor-query>` and it can build the query via the `name`s and  `value`s of those tags. You can also pass the `value` in via the inner text of the `<query-param>`.

```
<anchor-query href="http://www.facebook.com/sharer.php">
  <query-param name="p[url]" value="https://github.com/reggi/polymer-anchor-query"></query-param>
  <query-param name="p[images][0]" value="https://pbs.twimg.com/profile_images/436575110950948864/R8YcGKHV.png"></query-param>
  <query-param name="p[title]">Github polymer-anchor-query</query-param>
  <query-param name="p[summary]">Create an anchor and pass in the query parameters as HTML attributes.</query-param>
  <i class="fa fa-facebook"></i>
</anchor-query>
```

> **Note**: You can also mix query params from `<anchor-query>` attributes and the `<query-param>` tags. Query parms from the `<query-param>` tags will overwrite the attributes from `<anchor-query>`.

## Attributes

### `href` 
 
The base url. (required)