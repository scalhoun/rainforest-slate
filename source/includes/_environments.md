# Environments

## The Environments Object

```ruby
#<Rainforest::Environment:0x3ff73d710894 id=1> Attributes: {
  "created_at": "2015-03-18T01:13:52Z",
  "default": true,
  "id": 1,
  "name": "testing 123",
  "site_environments": [
    {"id":17,"created_at":"2015-07-01T01:08:51Z","site_id":10,"environment_id":1,"url":"http://www.test.com"},
    {"id":1,"created_at":"2015-03-18T01:13:52Z","site_id":1,"environment_id":1,"url":"https://www.apibits-test.com"}
  ],
  "webhook": "",
  "webhook_enabled": null
}
```

TODO: Fill this in.

Attributes |           |
---------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">string</div> | TODO: Add some info about the created_at attribute
**created_at** <div class="attr attr-type">datetime</div> | TODO: Add some info about the attribute
**default** <div class="attr attr-type">boolean</div> | TODO: Add some info about the attribute
**name** <div class="attr attr-type">string</div> | TODO: Add some info about the attribute
**site_environments** | TODO: Add some info about the attribute
**webhook** <div class="attr attr-type">string</div> | TODO: Add some info about the attribute
**webhook_enabled** <div class="attr attr-type">boolean</div> | TODO: Add some info about the attribute


## Create an Environment

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

env = Rainforest::Environment.create(
  :default => false,
  :name => "my testing environment"
)


EXAMPLE RESPONSE
#<Rainforest::Environment:0x3ff73d6c9d18 id=13> Attributes: {
  "created_at": "2015-07-22T18:16:25Z",
  "default": false,
  "id": 13,
  "name": "my testing environment",
  "site_environments": [
    {"id":24,"created_at":"2015-07-22T18:16:25Z","site_id":1,"environment_id":13,"url":"http://www.example.org"},
    {"id":23,"created_at":"2015-07-22T18:16:25Z","site_id":10,"environment_id":13,"url":"http://www.example.org"}
  ],
  "webhook": "",
  "webhook_enabled": null
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**default** <div class="attr attr-type">boolean</div> | Whether or not this environment should be the default environment.
**name** <div class="attr attr-type">string</div> | The name you want to use for this environment.


## Retrieve an Environment

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 13
env = Rainforest::Environment.retrieve(id)


EXAMPLE RESPONSE
#<Rainforest::Environment:0x3ff73d6c9d18 id=13> Attributes: {
  "created_at": "2015-07-22T18:16:25Z",
  "default": false,
  "id": 13,
  "name": "my testing environment",
  "site_environments": [
    {"id":24,"created_at":"2015-07-22T18:16:25Z","site_id":1,"environment_id":13,"url":"http://www.example.org"},
    {"id":23,"created_at":"2015-07-22T18:16:25Z","site_id":10,"environment_id":13,"url":"http://www.example.org"}
  ],
  "webhook": "",
  "webhook_enabled": null
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the environment you want to retrieve.


## Update an Environment

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 13
env = Rainforest::Environment.update(id, :name => "new env name")
# or
env = Rainforest::Environmnet.retrieve(id)
env.name = "new env name"
env.save


EXAMPLE RESPONSE
#<Rainforest::Environment:0x3ff73d6c9d18 id=13> Attributes: {
  "created_at": "2015-07-22T18:16:25Z",
  "default": false,
  "id": 13,
  "name": "my testing environment",
  "site_environments": [
    {"id":24,"created_at":"2015-07-22T18:16:25Z","site_id":1,"environment_id":13,"url":"http://www.example.org"},
    {"id":23,"created_at":"2015-07-22T18:16:25Z","site_id":10,"environment_id":13,"url":"http://www.example.org"}
  ],
  "webhook": "",
  "webhook_enabled": null
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the environment you want to retrieve.
**name** <div class="attr attr-type">integer</div> | The new name for the environment.

```ruby

```

TODO: Fill this in.


## List all Environments

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

envs = Rainforest::Environment.all

# The list is enumerable and works similarly to an array
envs.each do |env|
  # work with an environment
end

envs[0] # The first environment in the list
envs.length # the number of environments returns


EXAMPLE RESPONSE
#<Rainforest::ApiList[Rainforest::Environment]:0x3ff73d57a598> Data: [
  "#<Rainforest::Environment:0x3ff73d577dac id=13>"
]


```

TODO: Fill this in.
