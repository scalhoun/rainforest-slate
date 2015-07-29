# Runs

## The Run Object

```ruby
#<Rainforest::Run:0x3fdb69576b04 id=4268> Attributes: {
  "browsers": [
    {"name":"android_phone_landscape","state":"disabled","description":"Android Phone Landscape","category":"phone"},
    {"name":"android_phone_portrait","state":"disabled","description":"Android Phone Portrait","category":"phone"},
    {"name":"android_tablet_landscape","state":"disabled","description":"Android Tablet Landscape","category":"tablet"},
    {"name":"android_tablet_portrait","state":"disabled","description":"Android Tablet Portrait","category":"tablet"},
    {"name":"chrome","state":"enabled","description":"Google Chrome","category":"browser"},
    {"name":"firefox","state":"enabled","description":"Mozilla Firefox","category":"browser"},
    {"name":"ie8","state":"enabled","description":"Microsoft Internet Explorer 8","category":"browser"},
    {"name":"ie9","state":"enabled","description":"Microsoft Internet Explorer 9","category":"browser"},
    {"name":"ie10","state":"disabled","description":"Microsoft Internet Explorer 10","category":"browser"},
    {"name":"ie11","state":"disabled","description":"Microsoft Internet Explorer 11","category":"browser"},
    {"name":"safari","state":"enabled","description":"Apple Safari","category":"browser"}
  ],
  "created_at": "2013-11-14T04:52:14Z",
  "current_progress": {"percent":100,"total":5,"complete":5,"eta":{"seconds":0,"ts":"2015-07-27T18:33:20.841+00:00"},"no_result":0,"passed":0,"failed":1},
  "description": null,
  "environment": {"id":1144,"created_at":"2013-11-05T02:17:14Z","name":"Staging","default":true,"webhook":null,"webhook_enabled":null,"site_environments":[{"id":744,"created_at":"2013-11-05T02:17:14Z","site_id":860,"environment_id":1144,"url":"http://apibits.com"}]},
  "filters": null,
  "frontend_url": "https://app.rnfrst.com/runs/4268",
  "id": 4268,
  "log_url": null,
  "real_cost_to_run": 5,
  "result": "failed",
  "sample_test_titles": [
    "super awesome test"
  ],
  "state": "complete",
  "state_details": {"name":"complete","is_final_state":true},
  "stats": {"total_time_for_one_person":4675.0,"total_time_for_rainforest":2610.763738,"total_rainforest_overhead":13.591364,"speed_up":1.79},
  "timestamps": {"complete":"2013-11-14T05:35:45.022Z","in_progress":"2013-11-14T04:52:27.847Z","validating":"2013-11-14T04:52:28.003Z","created_at":"2013-11-14T04:52:14.252Z"},
  "total_failed_tests": 1,
  "total_no_result_tests": 0,
  "total_passed_tests": 0,
  "total_tests": 1
}
```

TODO: Fill this in.

Attributes |           |
---------- | --------- |
**browsers** <div class="attr attr-type">string</div> | TODO: Add some info about `browsers`
**created_at** <div class="attr attr-type">string</div> | TODO: Add some info about `created_at`
**current_progress** <div class="attr attr-type">string</div> | TODO: Add some info about `current_progress`
**description** <div class="attr attr-type">string</div> | TODO: Add some info about `description`
**environment** <div class="attr attr-type">string</div> | TODO: Add some info about `environment`
**filters** <div class="attr attr-type">string</div> | TODO: Add some info about `filters`
**frontend_url** <div class="attr attr-type">string</div> | TODO: Add some info about `frontend_url`
**id** <div class="attr attr-type">string</div> | TODO: Add some info about `id`
**log_url** <div class="attr attr-type">string</div> | TODO: Add some info about `log_url`
**real_cost_to_run** <div class="attr attr-type">string</div> | TODO: Add some info about `real_cost_to_run`
**result** <div class="attr attr-type">string</div> | TODO: Add some info about `result`
**sample_test_titles** <div class="attr attr-type">string</div> | TODO: Add some info about `sample_test_titles`
**state** <div class="attr attr-type">string</div> | TODO: Add some info about `state`
**state_details** <div class="attr attr-type">string</div> | TODO: Add some info about `state_details`
**stats** <div class="attr attr-type">string</div> | TODO: Add some info about `stats`
**timestamps** <div class="attr attr-type">string</div> | TODO: Add some info about `timestamps`
**total_failed_tests** <div class="attr attr-type">string</div> | TODO: Add some info about `total_failed_tests`
**total_no_result_tests** <div class="attr attr-type">string</div> | TODO: Add some info about `total_no_result_tests`
**total_passed_tests** <div class="attr attr-type">string</div> | TODO: Add some info about `total_passed_tests`
**total_tests** <div class="attr attr-type">string</div> | TODO: Add some info about `total_tests`



## Create a Run

> EXAMPLE REQUEST

> curl uses the -u flag to pass basic auth credentials (adding a colon after your API key will prevent it from asking you for a password).

> A sample test API key has been provided in all the examples on the page, so you can test out any example right away.

```ruby
require 'rainforest'
Rainforest.api_key = "your-api-key"

run = Rainforest::Run.create(
  :tags => ["www", "api"]
)
# or
test_ids = [2818]
run = Rainforest::Run.create(
  :tests => test_ids
)
```

> EXAMPLE RESPONSE

```ruby
#<Rainforest::Run:0x3fd87005e244 id=31061> Attributes: {
  "browsers": [
    {"name":"android_phone_landscape","state":"disabled","description":"Android Phone Landscape","category":"phone"},
    {"name":"android_phone_portrait","state":"disabled","description":"Android Phone Portrait","category":"phone"},
    {"name":"android_tablet_landscape","state":"disabled","description":"Android Tablet Landscape","category":"tablet"},
    {"name":"android_tablet_portrait","state":"disabled","description":"Android Tablet Portrait","category":"tablet"},
    {"name":"chrome","state":"disabled","description":"Google Chrome","category":"browser"},
    {"name":"firefox","state":"disabled","description":"Mozilla Firefox","category":"browser"},
    {"name":"ie8","state":"disabled","description":"Microsoft Internet Explorer 8","category":"browser"},
    {"name":"ie9","state":"disabled","description":"Microsoft Internet Explorer 9","category":"browser"},
    {"name":"ie10","state":"disabled","description":"Microsoft Internet Explorer 10","category":"browser"},
    {"name":"ie11","state":"disabled","description":"Microsoft Internet Explorer 11","category":"browser"},
    {"name":"safari","state":"disabled","description":"Apple Safari","category":"browser"}
  ],
  "created_at": "2015-07-28T16:52:55Z",
  "current_progress": {"percent":0,"total":0,"complete":0,"eta":{"seconds":1800,"ts":"2015-07-28T17:22:55.215+00:00"},"no_result":0,"passed":0,"failed":0},
  "description": null,
  "environment": {"id":1144,"created_at":"2013-11-05T02:17:14Z","name":"Staging","default":true,"webhook":null,"webhook_enabled":null,"site_environments":[{"id":744,"created_at":"2013-11-05T02:17:14Z","site_id":860,"environment_id":1144,"url":"http://blog.apibits.com"}]},
  "filters": {"tags":["www"]},
  "frontend_url": "https://app.rnfrst.com/runs/31061",
  "id": 31061,
  "log_url": null,
  "real_cost_to_run": 0,
  "result": "no_result",
  "sample_test_titles": [

  ],
  "state": "queued",
  "state_details": {"name":"queued","is_final_state":false},
  "stats": {"total_time_for_one_person":0.0,"total_time_for_rainforest":14400.0,"total_rainforest_overhead":0.0,"speed_up":0.0},
  "timestamps": {"created_at":"2015-07-28T16:52:55.126Z"},
  "total_failed_tests": 0,
  "total_no_result_tests": 0,
  "total_passed_tests": 0,
  "total_tests": 0,
  "requested_tests": [
    2181
  ]
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**tags** <div class="attr attr-required">required</div> <div class="attr attr-type">array</div> | The tags you would like to create a run with. *NOTE*: This is only required when `tests` is not provided.
**tests** <div class="attr attr-required">required</div> <div class="attr attr-type">array</div> | The ids of tests you would like to create runs with. *NOTE*: This is only required when `tags` is not provided.


## Retrieve a Run

> EXAMPLE REQUEST

```ruby
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 31061
run = Rainforest::Run.retrieve(id)
```

> EXAMPLE RESPONSE

```ruby
#<Rainforest::Run:0x3fd87005e244 id=31061> Attributes: {
  "browsers": [
    {"name":"android_phone_landscape","state":"disabled","description":"Android Phone Landscape","category":"phone"},
    {"name":"android_phone_portrait","state":"disabled","description":"Android Phone Portrait","category":"phone"},
    {"name":"android_tablet_landscape","state":"disabled","description":"Android Tablet Landscape","category":"tablet"},
    {"name":"android_tablet_portrait","state":"disabled","description":"Android Tablet Portrait","category":"tablet"},
    {"name":"chrome","state":"disabled","description":"Google Chrome","category":"browser"},
    {"name":"firefox","state":"disabled","description":"Mozilla Firefox","category":"browser"},
    {"name":"ie8","state":"disabled","description":"Microsoft Internet Explorer 8","category":"browser"},
    {"name":"ie9","state":"disabled","description":"Microsoft Internet Explorer 9","category":"browser"},
    {"name":"ie10","state":"disabled","description":"Microsoft Internet Explorer 10","category":"browser"},
    {"name":"ie11","state":"disabled","description":"Microsoft Internet Explorer 11","category":"browser"},
    {"name":"safari","state":"disabled","description":"Apple Safari","category":"browser"}
  ],
  "created_at": "2015-07-28T16:52:55Z",
  "current_progress": {"percent":0,"total":0,"complete":0,"eta":{"seconds":1800,"ts":"2015-07-28T17:22:55.215+00:00"},"no_result":0,"passed":0,"failed":0},
  "description": null,
  "environment": {"id":1144,"created_at":"2013-11-05T02:17:14Z","name":"Staging","default":true,"webhook":null,"webhook_enabled":null,"site_environments":[{"id":744,"created_at":"2013-11-05T02:17:14Z","site_id":860,"environment_id":1144,"url":"http://blog.apibits.com"}]},
  "filters": {"tags":["www"]},
  "frontend_url": "https://app.rnfrst.com/runs/31061",
  "id": 31061,
  "log_url": null,
  "real_cost_to_run": 0,
  "result": "no_result",
  "sample_test_titles": [

  ],
  "state": "queued",
  "state_details": {"name":"queued","is_final_state":false},
  "stats": {"total_time_for_one_person":0.0,"total_time_for_rainforest":14400.0,"total_rainforest_overhead":0.0,"speed_up":0.0},
  "timestamps": {"created_at":"2015-07-28T16:52:55.126Z"},
  "total_failed_tests": 0,
  "total_no_result_tests": 0,
  "total_passed_tests": 0,
  "total_tests": 0,
  "requested_tests": [
    2181
  ]
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the run you want to retrieve.


## List all Runs

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

runs = Rainforest::Run.all

# The list is enumerable and works similarly to a array
runs.each do |run|
  # work with a run
end

runs[0] # The first run in the list
runs.length # the number of runs returned


EXAMPLE RESPONSE
#<Rainforest::ApiList[Rainforest::Run]:0x3ff73d57a598> Data: [
  "#<Rainforest::Run:0x3ff73d577dac id=31061>",
  "#<Rainforest::Run:0x3ff73d661bb4 id=906>"
]


```

TODO: Fill this in.


## Abort or Delete a Run

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 31061
response = Rainforest::Run.abort(id) # or .delete(id)
# or
run = Rainforest::Run.retrieve(id)
run.abort # or .delete


EXAMPLE RESPONSE
#<Rainforest::Run:0x3fd87006c6dc id=31061> Attributes: {
  "browsers": [
    {"name":"android_phone_landscape","state":"disabled","description":"Android Phone Landscape","category":"phone"},
    {"name":"android_phone_portrait","state":"disabled","description":"Android Phone Portrait","category":"phone"},
    {"name":"android_tablet_landscape","state":"disabled","description":"Android Tablet Landscape","category":"tablet"},
    {"name":"android_tablet_portrait","state":"disabled","description":"Android Tablet Portrait","category":"tablet"},
    {"name":"chrome","state":"enabled","description":"Google Chrome","category":"browser"},
    {"name":"firefox","state":"enabled","description":"Mozilla Firefox","category":"browser"},
    {"name":"ie8","state":"disabled","description":"Microsoft Internet Explorer 8","category":"browser"},
    {"name":"ie9","state":"disabled","description":"Microsoft Internet Explorer 9","category":"browser"},
    {"name":"ie10","state":"disabled","description":"Microsoft Internet Explorer 10","category":"browser"},
    {"name":"ie11","state":"disabled","description":"Microsoft Internet Explorer 11","category":"browser"},
    {"name":"safari","state":"disabled","description":"Apple Safari","category":"browser"}
  ],
  "created_at": "2015-07-28T16:52:55Z",
  "current_progress": {"percent":0,"total":2,"complete":0,"eta":{"seconds":1800,"ts":"2015-07-28T17:25:59.042+00:00"},"no_result":1,"passed":0,"failed":0},
  "description": null,
  "environment": {"id":1144,"created_at":"2013-11-05T02:17:14Z","name":"Staging","default":true,"webhook":null,"webhook_enabled":null,"site_environments":[{"id":744,"created_at":"2013-11-05T02:17:14Z","site_id":860,"environment_id":1144,"url":"http://blog.apibits.com"}]},
  "filters": {"tags":["www"]},
  "frontend_url": "https://app.rnfrst.com/runs/31061",
  "id": 31061,
  "log_url": null,
  "real_cost_to_run": 2,
  "result": "no_result",
  "sample_test_titles": [
    "Jon's Test"
  ],
  "state": "in_progress",
  "state_details": {"name":"in_progress","is_final_state":false},
  "stats": {"total_time_for_one_person":0.0,"total_time_for_rainforest":4.874452,"total_rainforest_overhead":4.874452,"speed_up":0.0},
  "timestamps": {"in_progress":"2015-07-28T16:53:00.024Z","validating":"2015-07-28T16:52:57.487Z","created_at":"2015-07-28T16:52:55.126Z"},
  "total_failed_tests": 0,
  "total_no_result_tests": 1,
  "total_passed_tests": 0,
  "total_tests": 1,
  "requested_tests": null
}
```

TODO: Fill this in.


## List a Run's Tests

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 905
run = Rainforest::Run.retrieve(id)
tests = run.tests.all
# or
tests = Rainforest::Run.new(id).tests.all


EXAMPLE RESPONSE
#<Rainforest::ApiList[Rainforest::Test]:0x3fd86fdf11f0> Data: [
  "#<Rainforest::Test:0x3fd86fdf0bc4 id=2181>"
]

```

TODO: Fill this in.
