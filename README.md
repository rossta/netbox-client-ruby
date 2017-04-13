# Netbox::Client::Ruby

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/netbox/client/ruby`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## TODO

* Complete usage in Readme
* Complete description in Readme
* Implement pagination
* Implement creation of objects

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'netbox-client-ruby'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install netbox-client-ruby

## Usage

### Configuration

Put this somewhere, where it runs, before any call to anything else of Cloudflair.
If you are using Rails, then this would probably be somewhere underneath /config.

```ruby
require 'netbox-client-ruby'
NetboxClientRuby.configure do |config|
  config.netbox.auth.token = 'YOUR_API_TOKEN'
  config.netbox.api_base_url = 'http://netbox.local/api/'

  # these are optional:
  config.netbox.pagination.default_limit = 50
  config.faraday.adapter = Faraday.default_adapter
  config.faraday.request_options = { open_timeout: 1, timeout: 5 }
  config.faraday.logger = :logger # built-in options: :logger, :detailed_logger; default: nil
end
```


## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/ninech/netbox-client-ruby.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

