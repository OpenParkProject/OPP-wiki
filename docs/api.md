# API Documentation

APIs are specified in [OPP-common](https://github.com/OpenParkProject/OPP-common/openapi.yaml) repository in OpenAPI 3.1 format.
The OpenAPI spec is used to generate the API documentation as well as the server and client stubs with request validation and authentication as a single source of truth.

## OpenAPI spec

<div id="redoc-wrapper">
  <div id="redoc-container"></div>
</div>

<script src="https://cdn.redoc.ly/redoc/latest/bundles/redoc.standalone.js"></script>
<script>
  Redoc.init('../openapi.yaml', {}, document.getElementById('redoc-container'));
</script>

<style>
  html, body {
    height: 100%;
    margin: 0;
  }

  #redoc-wrapper {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  #redoc-container {
    flex: 1;
    width: 170%;
    margin: 0 auto;
  }

  footer {
    z-index: 10;
  }
</style>
