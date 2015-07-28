# Pagination

```ruby
require 'rainforest'
Rainforest.api_key = 'your-api-key'

runs_pg_2 = Rainforest::Run.all(:page => 2)
```

Nearly all API calls used to list a resource support pagination. To specify your page simply pass in the `page` parameter.
