# Generators

## The Generator Object

```ruby
#<Rainforest::Generator:0x3ff73f454004 id=905> Attributes: {
  "columns": [
    {"id":6440,"created_at":"2015-07-27T16:52:13Z","name":"first_name"},
    {"id":6441,"created_at":"2015-07-27T16:52:13Z","name":"last_name"},
    {"id":6442,"created_at":"2015-07-27T16:52:13Z","name":"email"},
    {"id":6443,"created_at":"2015-07-27T16:52:13Z","name":"passwword"}
  ],
  "created_at": "2015-07-27T16:52:13Z",
  "description": "Credentials used to log into accounts in various states",
  "generator_type": "tabular",
  "id": 905,
  "name": "user_credentials",
  "row_count": 2
}
```

TODO: Fill this in.

Attributes |           |
---------- | --------- |
**id** <div class="attr attr-type">string</div> | TODO: Add some info about the created_at attribute
**created_at** <div class="attr attr-type">datetime</div> | TODO: Add some info about the attribute
**name** <div class="attr attr-type">string</div> | TODO: Add some info about the attribute
**description** <div class="attr attr-type">string</div> | TODO: Add some info about the attribute
**columns** | TODO: Add some info about the attribute
**generator_type** <div class="attr attr-type">string</div> | TODO: Add some info about the attribute
**row_count** <div class="attr attr-type">integer</div> | TODO: Add some info about the attribute


## Create a Generator

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

gen = Rainforest::Generator.create(
  :name => "user_credentials",
  :description => "Credentials used to log into accounts in various states",
  :columns => ["first_name", "last_name", "email", "passwword"]
)


EXAMPLE RESPONSE
#<Rainforest::Generator:0x3ff73f514d40 id=906> Attributes: {
  "columns": [
    {"id":6444,"created_at":"2015-07-27T17:00:22Z","name":"first_name"},
    {"id":6445,"created_at":"2015-07-27T17:00:22Z","name":"last_name"},
    {"id":6446,"created_at":"2015-07-27T17:00:22Z","name":"email"},
    {"id":6447,"created_at":"2015-07-27T17:00:22Z","name":"passwword"}
  ],
  "created_at": "2015-07-27T17:00:22Z",
  "data": null,
  "description": "Credentials used to log into accounts in various states",
  "generator_type": "tabular",
  "id": 906,
  "name": "user_credentials_1",
  "row_count": 0
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**name** <div class="attr attr-required">required</div> <div class="attr attr-type">string</div> | The name you wat to use for this generator. Ca only include letters, numbers, ad underscores.
**description** <div class="attr attr-type">string</div> | The human readable description of what this generator is used for.
**columns** <div class="attr attr-type">array[string]</div> | An array of column names used with this generator.


## Retrieve a Generator

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 905
gen = Rainforest::Generator.retrieve(id)


EXAMPLE RESPONSE
#<Rainforest::Generator:0x3ff73fcbdfb0 id=905> Attributes: {
  "columns": [
    {"id":6440,"created_at":"2015-07-27T16:52:13Z","name":"first_name"},
    {"id":6441,"created_at":"2015-07-27T16:52:13Z","name":"last_name"},
    {"id":6442,"created_at":"2015-07-27T16:52:13Z","name":"email"},
    {"id":6443,"created_at":"2015-07-27T16:52:13Z","name":"passwword"}
  ],
  "created_at": "2015-07-27T16:52:13Z",
  "data": null,
  "description": "Credentials used to log into accounts in various states",
  "generator_type": "tabular",
  "id": 905,
  "name": "user_credentials",
  "row_count": 2
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the generator you wat to retrieve.


## Update a Generator

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 905
gen = Rainforest::Generator.update(id, {
  :name => "new_gen_name",
  :description => "Credentials used to log into accounts in various states"
})
# or
gen = Rainforest::Generator.retrieve(id)
gen.name = "new_gen_name"
gen.save


EXAMPLE RESPONSE
#<Rainforest::Generator:0x3fdb68e27b8c id=905> Attributes: {
  "columns": [
    {"id":6440,"created_at":"2015-07-27T16:52:13Z","name":"first_name"},
    {"id":6441,"created_at":"2015-07-27T16:52:13Z","name":"last_name"},
    {"id":6442,"created_at":"2015-07-27T16:52:13Z","name":"email"},
    {"id":6443,"created_at":"2015-07-27T16:52:13Z","name":"passwword"}
  ],
  "created_at": "2015-07-27T16:52:13Z",
  "description": "Credentials used to log into accounts in various states",
  "generator_type": "tabular",
  "id": 905,
  "name": "user_creds",
  "row_count": 2
}
```

TODO: Fill this in.


Arguments |           |
--------- | --------- |
**id** <div class="attr attr-required">required</div> <div class="attr attr-type">integer</div> | The id of the generator you wat to update.


Editable Attributes |           |
------------------- | --------- |
**name** <div class="attr attr-required">required</div> <div class="attr attr-type">string</div> | The name of the generator. Ca only include letters, numbers, ad underscores.
**description** <div class="attr attr-required">required</div> <div class="attr attr-type">string</div> | The description of the generator.



## List all Generators

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

gens = Rainforest::Generator.all

# The list is enumerable ad works similarly to a array
gens.each do |gen|
  # work with a generator
end

gens[0] # The first generator in the list
gens.length # the number of generators returned


EXAMPLE RESPONSE
#<Rainforest::ApiList[Rainforest::Generator]:0x3ff73d57a598> Data: [
  "#<Rainforest::Generator:0x3ff73d577dac id=905>",
  "#<Rainforest::Generator:0x3ff73d661bb4 id=906>"
]


```

TODO: Fill this in.


## Delete a Generator

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 906
response = Rainforest::Generator.delete(id)
# or
env = Rainforest::Generator.retrieve(id)
env.delete


EXAMPLE RESPONSE
#<Rainforest::Generator:0x3fdb6955ba70 id=906> Attributes: {
  "columns": [
    {"id":6444,"created_at":"2015-07-27T17:00:22Z","name":"first_name"},
    {"id":6445,"created_at":"2015-07-27T17:00:22Z","name":"last_name"},
    {"id":6446,"created_at":"2015-07-27T17:00:22Z","name":"email"},
    {"id":6447,"created_at":"2015-07-27T17:00:22Z","name":"passwword"}
  ],
  "created_at": "2015-07-27T17:00:22Z",
  "description": "Credentials used to log into accounts in various states",
  "generator_type": "tabular",
  "id": 906,
  "name": "user_credentials_1",
  "row_count": 0
}

```

TODO: Fill this in.


## List a Generator's Rows

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 905
gen = Rainforest::Generator.retrieve(id)
rows = gen.rows.all
# or
rows = Rainforest::Generator.new(id).rows.all


EXAMPLE RESPONSE
[
  {
    :id => 113914,
    :data => {
      :"6440" => "Jon",
      :"6441" => "Calhoun",
      :"6442" => "sample@apibits.com",
      :"6443" => "someSUPERs3cr3tPASSword"
    }
  },
  {
    :id => 113915,
    :data => {
      :"6440" => "Pam",
      :"6441" => "Beesly",
      :"6442" => "pam@apibits.com",
      :"6443" => "dundies are great"
    }
  }
]


```

TODO: Fill this in.

## Create a Generator Row

```ruby
EXAMPLE REQUEST
require 'rainforest'
Rainforest.api_key = "your-api-key"

id = 905
gen = Rainforest::Generator.retrieve(id)
row = gen.rows.create(
  :data => {
    6440 => "Jerry", # 6440 is the column id from gen.columns
    6441 => "Seinfeld",
    6442 => "jerry@apibits.com",
    6443 => "fake_password_123"
  }
)
# or
row = Rainforest::Generator.new(id).rows.create(
  :data => {
    6440 => "Jerry", # 6440 is the column id from gen.columns
    6441 => "Seinfeld",
    6442 => "jerry@apibits.com",
    6443 => "fake_password_123"
  }
)


EXAMPLE RESPONSE
{
  :id => 113916,
  :data => {
    :"6440" => "Jerry",
    :"6441" => "Seinfeld",
    :"6442" => "jerry@apibits.com",
    :"6443" => "fake_password_123"
  }
}


```

TODO: Fill this in.
