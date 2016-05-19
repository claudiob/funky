# Funky

Under the hood, Funky hits FB's APIs on most cases, while other cases it will scrape FB's HTML to get the data. It's kind of... funky.

## Usage

Right now it can only be used to get basic count data of Facebook videos.

```ruby
ids = ['10154439119663508', '10153834590672139']
fb = Funky::Video.where(ids: ids, fields: ['likes.summary(true)', [comments.summary(true)]])
videos.first.like_count    #=> 1169
videos.first.comment_count #=> 65
videos.first.share_count   #=> 348
videos.first.view_count    #=> 10121

```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/funky. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

