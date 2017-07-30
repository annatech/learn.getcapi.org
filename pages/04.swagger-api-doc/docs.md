---
title: 'Swagger API Doc'
process:
    markdown: true
    twig: true
twig_first: true
---

{% block stylesheets %}
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700|Source+Code+Pro:300,600|Titillium+Web:400,600,700" rel="stylesheet">
<link rel="stylesheet" type="text/css" href="/swagger-ui-master/dist/swagger-ui.css" >

<style>
    html
    {
        box-sizing: border-box;
        overflow: -moz-scrollbars-vertical;
        overflow-y: scroll;
    }
    *,
    *:before,
    *:after
    {
        box-sizing: inherit;
    }

    body {
      margin:0;
      background: #fafafa;
    }
  </style>

{% endblock %}

<div id="swagger-ui"></div>

<script src="/swagger-ui-master/dist/swagger-ui-bundle.js"> </script>
<script src="/swagger-ui-master/dist/swagger-ui-standalone-preset.js"> </script>
<script>
window.onload = function() {
  // Build a system
  const ui = SwaggerUIBundle({
    url: "https://getcapi.io/api/v1/slim/swagger",
    dom_id: '#swagger-ui',
    deepLinking: true,
    presets: [
      SwaggerUIBundle.presets.apis,
      SwaggerUIStandalonePreset
    ],
    plugins: [
      SwaggerUIBundle.plugins.DownloadUrl
    ],
  })
  window.ui = ui
}
</script>
<!--
<iframe onload="iFrameHeight()"	id="blockrandom" name="iframe" src="/swagger-ui-master/dist/" width="100%" height="900" scrolling="auto" frameborder="0" class="wrapper"> This option will not work correctly. Unfortunately, your browser does not support inline frames.</iframe>
-->