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

**Attributes**

Parameter | Description
--------- | -----------
id | **string**
created_at | TODO
default | TODO
name | TODO
site_environments | TODO
webhook | TODO
webhook_enabled | TODO


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


**Arguments**

Parameter | Description
--------- | -----------
default | **boolean** Whether or not this environment should be the default environment.
name | **string** The name you want to use for this environment.


## Retrieve an Environment

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

env_id = 13
env = Rainforest::Environment.retrieve(env_id)


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


**Arguments**

Parameter | Description
--------- | -----------
id | **integer** The id of the environment you want to retrieve.


## Update an Environment

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

env_id = 13
env = Rainforest::Environment.update(env_id, :name => "new env name")
# or
env = Rainforest::Environmnet.retrieve(env_id)
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


**Arguments**

Parameter | Description
--------- | -----------
name | **integer** The id of the environment you want to retrieve.

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
