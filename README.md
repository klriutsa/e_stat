# EStat

e_stat API Wrapper
http://www.e-stat.go.jp/api/

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'e_stat'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install e_stat

## Usage

Get API key
http://www.e-stat.go.jp/api/

```ruby
key = 'api_key'
estat = EStat::API.new(key)
res = estat.get_stats_list('0201', '00200521', survey_years: '2000', start_position: '1')
estat.get_meta_info(res.first['@id'])
estat.get_stats_data(res.first['@id'])
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/klriutsa/e_stat. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
