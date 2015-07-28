# Tests

## The Test Object

```ruby
#<Rainforest::Test:0x3fd86d602270 id=17790> Attributes: {
  "browsers": [
    {"name":"android_phone_landscape","description":"Android Phone Landscape","category":"phone","state":"disabled"},
    {"name":"android_phone_portrait","description":"Android Phone Portrait","category":"phone","state":"disabled"},
    {"name":"android_tablet_landscape","description":"Android Tablet Landscape","category":"tablet","state":"disabled"},
    {"name":"android_tablet_portrait","description":"Android Tablet Portrait","category":"tablet","state":"disabled"},
    {"name":"chrome","description":"Google Chrome","category":"browser","state":"enabled"},
    {"name":"firefox","description":"Mozilla Firefox","category":"browser","state":"disabled"},
    {"name":"ie8","description":"Microsoft Internet Explorer 8","category":"browser","state":"disabled"},
    {"name":"ie9","description":"Microsoft Internet Explorer 9","category":"browser","state":"disabled"},
    {"name":"ie10","description":"Microsoft Internet Explorer 10","category":"browser","state":"disabled"},
    {"name":"ie11","description":"Microsoft Internet Explorer 11","category":"browser","state":"disabled"},
    {"name":"safari","description":"Apple Safari","category":"browser","state":"disabled"}
  ],
  "created_at": "2015-07-28T15:02:00Z",
  "deletable": true,
  "deleted": false,
  "description": "Make sure all customer logos link to their websites correctly.",
  "dry_run_url": "https://tester.rainforestqa.com/tester/dry_run/vUu916ScjlWRwZbITsVnRg?turkSubmitTo=%2Fthanks",
  "editable": true,
  "has_been_dry_run": true,
  "id": 17790,
  "last_run": {"id":31459,"created_at":"2015-07-28T15:10:06Z","state":"complete"},
  "result": "passed",
  "run_mode": "default",
  "site_id": 860,
  "start_uri": "/",
  "step_count": 1,
  "tags": [
    "www"
  ],
  "test_id": 17790,
  "title": "Customer Logos",
  "quality": "acceptable"
}
```

TODO: Fill this in.

Attributes |           |
---------- | --------- |
**browsers** <div class="attr attr-type">string</div> | TODO: Add some info about `browsers`
**created_at** <div class="attr attr-type">string</div> | TODO: Add some info about `created_at`
**deletable** <div class="attr attr-type">string</div> | TODO: Add some info about `deletable`
**deleted** <div class="attr attr-type">string</div> | TODO: Add some info about `deleted`
**description** <div class="attr attr-type">string</div> | TODO: Add some info about `description`
**dry_run_url** <div class="attr attr-type">string</div> | TODO: Add some info about `dry_run_url`
**editable** <div class="attr attr-type">string</div> | TODO: Add some info about `editable`
**elements** <div class="attr attr-type">array</div> | TODO: Add some info about `elements`
**has_been_dry_run** <div class="attr attr-type">string</div> | TODO: Add some info about `has_been_dry_run`
**id** <div class="attr attr-type">string</div> | TODO: Add some info about `id`
**last_run** <div class="attr attr-type">string</div> | TODO: Add some info about `last_run`
**result** <div class="attr attr-type">string</div> | TODO: Add some info about `result`
**run_mode** <div class="attr attr-type">string</div> | TODO: Add some info about `run_mode`
**site_id** <div class="attr attr-type">string</div> | TODO: Add some info about `site_id`
**start_uri** <div class="attr attr-type">string</div> | TODO: Add some info about `start_uri`
**step_count** <div class="attr attr-type">string</div> | TODO: Add some info about `step_count`
**tags** <div class="attr attr-type">string</div> | TODO: Add some info about `tags`
**test_id** <div class="attr attr-type">string</div> | TODO: Add some info about `test_id`
**title** <div class="attr attr-type">string</div> | TODO: Add some info about `title`
**state** <div class="attr attr-type">string</div> | TODO: Add some info about `state`
**quality** <div class="attr attr-type">string</div> | TODO: Add some info about `quality`



## Create a Test

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"


test = Rainforest::Test.create(
  :start_uri => "/login",
  :title => "Log in to an account",
  :elements => [
    {
      :type => "step",
      :redirection=>true,
      :element => {
        :action => "Type 'test@apibits.com' into the email field, and 'password123' into the password field, then hit the log in button.",
        :response => "Were you redirected to the dashboard?"
      }
    }
  ]
)

EXAMPLE RESPONSE
#<Rainforest::Test:0x3ff930d38a74 id=17609> Attributes: {
  "browsers": [
    {"name":"android_phone_landscape","description":"Android Phone Landscape","category":"phone","state":"enabled"},
    {"name":"android_phone_portrait","description":"Android Phone Portrait","category":"phone","state":"enabled"},
    {"name":"android_tablet_landscape","description":"Android Tablet Landscape","category":"tablet","state":"enabled"},
    {"name":"android_tablet_portrait","description":"Android Tablet Portrait","category":"tablet","state":"enabled"},
    {"name":"chrome","description":"Google Chrome","category":"browser","state":"enabled"},
    {"name":"firefox","description":"Mozilla Firefox","category":"browser","state":"enabled"},
    {"name":"ie8","description":"Microsoft Internet Explorer 8","category":"browser","state":"enabled"},
    {"name":"ie9","description":"Microsoft Internet Explorer 9","category":"browser","state":"enabled"},
    {"name":"ie10","description":"Microsoft Internet Explorer 10","category":"browser","state":"enabled"},
    {"name":"ie11","description":"Microsoft Internet Explorer 11","category":"browser","state":"enabled"},
    {"name":"safari","description":"Apple Safari","category":"browser","state":"disabled"}
  ],
  "created_at": "2015-07-28T17:34:38Z",
  "deletable": true,
  "deleted": false,
  "description": null,
  "dry_run_url": "https://tester.rnfrst.com/tester/dry_run/kcVBInd0jUW_ELLk4NHTYg?turkSubmitTo=%2Fthanks",
  "editable": true,
  "has_been_dry_run": false,
  "id": 17609,
  "last_run": null,
  "result": "no_result",
  "run_mode": "default",
  "site_id": 860,
  "start_uri": "/login",
  "step_count": 1,
  "tags": [

  ],
  "test_id": 17609,
  "title": "Log in to an account",
  "quality": "no_data",
  "elements": [
    {"id":54913,"created_at":"2015-07-28T17:34:39Z","redirection":true,"type":"step","element":{"id":47999,"created_at":"2015-07-28T17:34:39Z","action":"Type 'test@apibits.com' into the email field, and 'password123' into the password field, then hit the log in button.","response":"Were you redirected to the dashboard?","browsers":null}}
  ],
  "attached_to": null
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**start_uri** <div class="attr attr-required">required</div> <div class="attr attr-type">string</div> | TODO: Fill this in.


## Retrieve a Test

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 905
test = Rainforest::Test.retrieve(id)


EXAMPLE RESPONSE
#<Rainforest::Test:0x3ff931d22ac0 id=17609> Attributes: {
  "browsers": [
    {"name":"android_phone_landscape","description":"Android Phone Landscape","category":"phone","state":"enabled"},
    {"name":"android_phone_portrait","description":"Android Phone Portrait","category":"phone","state":"enabled"},
    {"name":"android_tablet_landscape","description":"Android Tablet Landscape","category":"tablet","state":"enabled"},
    {"name":"android_tablet_portrait","description":"Android Tablet Portrait","category":"tablet","state":"enabled"},
    {"name":"chrome","description":"Google Chrome","category":"browser","state":"enabled"},
    {"name":"firefox","description":"Mozilla Firefox","category":"browser","state":"enabled"},
    {"name":"ie8","description":"Microsoft Internet Explorer 8","category":"browser","state":"enabled"},
    {"name":"ie9","description":"Microsoft Internet Explorer 9","category":"browser","state":"enabled"},
    {"name":"ie10","description":"Microsoft Internet Explorer 10","category":"browser","state":"enabled"},
    {"name":"ie11","description":"Microsoft Internet Explorer 11","category":"browser","state":"enabled"},
    {"name":"safari","description":"Apple Safari","category":"browser","state":"disabled"}
  ],
  "created_at": "2015-07-28T17:34:38Z",
  "deletable": true,
  "deleted": false,
  "description": null,
  "dry_run_url": "https://tester.rnfrst.com/tester/dry_run/kcVBInd0jUW_ELLk4NHTYg?turkSubmitTo=%2Fthanks",
  "editable": true,
  "has_been_dry_run": true,
  "id": 17609,
  "last_run": null,
  "result": "no_result",
  "run_mode": "default",
  "site_id": 860,
  "start_uri": "/login",
  "step_count": 1,
  "tags": [

  ],
  "test_id": 17609,
  "title": "Log in to an account",
  "quality": "no_data",
  "elements": [
    {"id":54913,"created_at":"2015-07-28T17:34:39Z","redirection":true,"type":"step","element":{"id":47999,"created_at":"2015-07-28T17:34:39Z","action":"Type 'test@apibits.com' into the email field, and 'password123' into the password field, then hit the log in button.","response":"Were you redirected to the dashboard?","browsers":null}}
  ],
  "attached_to": [

  ]
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the test you want to retrieve.


## Update a Test

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

# TODO: Fill this in
id = 17609
test = Rainforest::Test.update(id, :title => "New Test Title")
# or
test = Rainforest::Test.retrieve(id)
test.title = "New Test Title"
test.save


EXAMPLE RESPONSE
#<Rainforest::Test:0x3ff73d6c9d18 id=13> Attributes: {
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the test you want to update.

## List all Tests

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

tests = Rainforest::Test.all

# The list is enumerable and works similarly to a array
tests.each do |test|
  # work with a test
end

tests[0] # The first test in the list
tests.length # the number of tests returned


EXAMPLE RESPONSE
#<Rainforest::ApiList[Rainforest::Test]:0x3ff73d57a598> Data: [
  "#<Rainforest::Test:0x3ff73d577dac id=905>",
  "#<Rainforest::Test:0x3ff73d661bb4 id=2181>"
]


```

TODO: Fill this in.


## Delete a Test

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 17608
response = Rainforest::Test.delete(id)
# or
test = Rainforest::Test.retrieve(id)
test.delete


EXAMPLE RESPONSE
#<Rainforest::Test:0x3fdb6955ba70 id=906> Attributes: {
}

```

TODO: Fill this in.



## List a Test's History

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 13
test = Rainforest::Test.retrieve(id)
runs = test.history
# or
runs = Rainforest::Environment.new(id).history

# The list is enumerable and works similarly to an array
runs.each do |run|
  # work with an run
end

runs[0] # The first run in the list
runs.length # the number of runs


EXAMPLE RESPONSE
<Rainforest::ApiList[Rainforest::Run]:0x3ff73d6a52ec> Data: [
  "#<Rainforest::Run:0x3ff73d678e90 id=4138>",
  "#<Rainforest::Run:0x3ff73d661bb4 id=4242>"
]


```

A test's history is a list of runs associated with that test.

TODO: Finish this.
