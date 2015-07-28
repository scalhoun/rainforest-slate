---
title: API Reference

language_tabs:
  - ruby

toc_footers:
  - <a href='https://app.rnfrst.com/settings/integrations'>Where is my API Key?</a>
  - <a href='http://apibits.com'>API Libs by Apibits</a>


includes:
  - environments
  - generators
  - runs
  - schedules
  - tests

search: true
---

# Introduction

Welcome to the Rainforest API.

## Authentication

```ruby
require 'rainforest'
Rainforest.api_key = 'your-api-key'
```

> Make sure to replace `your-api-key` with your API key.

Rainforest uses API keys to allow access to the API. You can find your API key in the [integrations](https://app.rnfrst.com/settings/integrations) section of Rainforest.


## Pagination

```ruby
require 'rainforest'
Rainforest.api_key = 'your-api-key'

runs_pg_2 = Rainforest::Run.all(:page => 2)
```

Nearly all API calls used to list a resource support pagination. To specify your page simply pass in the `page` parameter.
