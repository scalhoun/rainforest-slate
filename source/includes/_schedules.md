# Schedules

## The Schedule Object

```ruby
#<Rainforest::Schedule:0x3fdcc6185a3c id=4> Attributes: {
  "created_at": "2015-03-25T00:19:56Z",
  "filters": {"tests":["all"]},
  "id": 4,
  "repeat_rules": [
    {"id":8,"created_at":"2015-03-25T00:19:56Z","day":"wednesday","time":"01:01"},
    {"id":7,"created_at":"2015-03-25T00:19:56Z","day":"monday","time":"01:01"},
    {"id":6,"created_at":"2015-03-25T00:19:56Z","day":"sunday","time":"01:01"}
  ]
}
```

TODO: Fill this in.

Attributes |           |
---------- | --------- |
**created_at** <div class="attr attr-type">string</div> | TODO: Add some info about `created_at`
**filters** <div class="attr attr-type">string</div> | TODO: Add some info about `filters`
**id** <div class="attr attr-type">string</div> | TODO: Add some info about `id`
**repeat_rules** <div class="attr attr-type">string</div> | TODO: Add some info about `repeat_rules`


## Create a Schedule

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

schedule = Rainforest::Schedule.create(
  :filters => {
    :tags => ["www"]
  },
  :repeat_rules => [
    {
      :day => "sunday",
      :time => "01:00"
    },
    {
      :day => "tuesday",
      :time => "10:00"
    }
  ]
)

EXAMPLE RESPONSE
#<Rainforest::Schedule:0x3fd870165f98 id=222> Attributes: {
  "created_at": "2015-07-28T17:01:43Z",
  "filters": {"tags":["www"]},
  "id": 222,
  "repeat_rules": [
    {"id":945,"created_at":"2015-07-28T17:01:43Z","day":"tuesday","time":"10:00"},
    {"id":944,"created_at":"2015-07-28T17:01:43Z","day":"sunday","time":"01:00"}
  ]
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**filters** <div class="attr attr-required">required</div> <div class="attr attr-type">array</div> | TODO: Fill this in.
**repeat_rules** <div class="attr attr-required">required</div> <div class="attr attr-type">array</div> | TODO: Fill this in.


## Retrieve a Schedule

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 222
schedule = Rainforest::Schedule.retrieve(id)


EXAMPLE RESPONSE
#<Rainforest::Schedule:0x3fd870165f98 id=222> Attributes: {
  "created_at": "2015-07-28T17:01:43Z",
  "filters": {"tags":["www"]},
  "id": 222,
  "repeat_rules": [
    {"id":945,"created_at":"2015-07-28T17:01:43Z","day":"tuesday","time":"10:00"},
    {"id":944,"created_at":"2015-07-28T17:01:43Z","day":"sunday","time":"01:00"}
  ]
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the schedule you want to retrieve.


## Update a Schedule

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 222
repeat_rules = [{:day => "monday", :time => "12:00"}]
schedule = Rainforest::Schedule.update(id, :repeat_rules => repeat_rules)
# or
schedule = Rainforest::Schedule.retrieve(id)
schedule.repeat_rules = repeat_rules
schedule.save


EXAMPLE RESPONSE
#<Rainforest::Schedule:0x3fd8701bddec id=222> Attributes: {
  "created_at": "2015-07-28T17:01:43Z",
  "filters": {"tags":["www"]},
  "id": 222,
  "repeat_rules": [
    {"id":946,"created_at":"2015-07-28T17:06:08Z","day":"monday","time":"12:00"}
  ]
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the schedule you want to update.
**repeat_rules** <div class="attr attr-type">array[repeat_rule]</div> | TODO: Fill this in.
**filters** <div class="attr attr-type">hash</div> | TODO: Fill this in.

## List all Schedules

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

schedules = Rainforest::Schedule.all

# The list is enumerable and works similarly to a array
schedules.each do |schedule|
  # work with a schedule
end

schedules[0] # The first schedule in the list
schedules.length # the number of schedules returned


EXAMPLE RESPONSE
#<Rainforest::ApiList[Rainforest::Schedule]:0x3ff73d57a598> Data: [
  "#<Rainforest::Schedule:0x3ff73d577dac id=905>",
  "#<Rainforest::Schedule:0x3ff73d661bb4 id=906>"
]


```

TODO: Fill this in.


## Delete a Schedule

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 223
response = Rainforest::Schedule.delete(id)
# or
schedule = Rainforest::Schedule.retrieve(id)
schedule.delete


EXAMPLE RESPONSE
#<Rainforest::Schedule:0x3ff930ff8930 id=223> Attributes: {
  "created_at": "2015-07-28T17:11:54Z",
  "filters": {"tags":["www"]},
  "id": 223,
  "repeat_rules": [
    {"id":950,"created_at":"2015-07-28T17:11:54Z","day":"tuesday","time":"10:00"},
    {"id":949,"created_at":"2015-07-28T17:11:54Z","day":"sunday","time":"01:00"}
  ]
}

```

TODO: Fill this in.


