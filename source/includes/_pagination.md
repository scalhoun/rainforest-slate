# Pagination

```ruby
require 'rainforest'
Rainforest.api_key = 'your-api-key'

runs_pg_2 = Rainforest::Run.all(:page => 2)
```

Nearly all API calls used to list a resource support pagination. To specify your page simply pass in the `page` parameter.

You can also set the `page_size` to determine how many resources will be included in each page. For example

```ruby
require 'rainforest'
Rainforst.api_key = 'your-api-key'

runs = Rainforest::Run.all(:page_size => 25)
```
