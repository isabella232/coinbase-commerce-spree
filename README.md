# SpreeCoinbaseCommerce

Accept crypto payments on your Spree store with the official Coinbase Commerce Spree plugin. 

## Installation

1. Add this extension to your Gemfile with this line:
  ```ruby
  gem 'spree_coinbase_commerce', github: 'coinbase/coinbase-commerce-spree'
  gem 'coinbase_commerce', github: 'coinbase/coinbase-commerce-ruby'
  ```

2. Install the gem using Bundler:
  ```ruby
  bundle install
  ```

3. Copy & run migrations
  ```ruby
  bundle exec rails g spree_coinbase_commerce:install
  ```
4. Add ```<your_spree_host>/spree_coinbase/notify``` to Coinbase Commerce webhook settings

5. Restart your server

  If your server was running, restart it so that it can find the assets properly.

## Testing

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

When testing your applications integration with this extension you may use it's factories.
Simply add this require statement to your spec_helper:

```ruby
require 'spree_coinbase_commerce/factories'
```

## Integrate with other e-commerce platforms
[Coinbase Commerce Integrations](https://commerce.coinbase.com/integrate)


Copyright (c) 2018 Coinbase Commerce, released under the New BSD License
