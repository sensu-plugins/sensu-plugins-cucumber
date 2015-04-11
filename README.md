## Sensu-Plugins-cucumber

[![Build Status](https://travis-ci.org/sensu-plugins/sensu-plugins-cucumber.svg?branch=master)](https://travis-ci.org/sensu-plugins/sensu-plugins-cucumber)
[![Gem Version](https://badge.fury.io/rb/sensu-plugins-cucumber.svg)](http://badge.fury.io/rb/sensu-plugins-cucumber)
[![Code Climate](https://codeclimate.com/github/sensu-plugins/sensu-plugins-cucumber/badges/gpa.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-cucumber)
[![Test Coverage](https://codeclimate.com/github/sensu-plugins/sensu-plugins-cucumber/badges/coverage.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-cucumber)
[![Dependency Status](https://gemnasium.com/sensu-plugins/sensu-plugins-cucumber.svg)](https://gemnasium.com/sensu-plugins/sensu-plugins-cucumber)

## Functionality

## Files
 * bin.check-cucumber
 *
 *
 *

## Usage

Example check_cucumber.json:

``` json
{
  "checks": {
    "check_cucumber_example": {
      "handlers": ["default"],
      "command": "check-cucumber.rb --name cucumber-example --handler cucumber --metric-handler metrics --metric-prefix example-metrics-prefix --command \"cucumber-js -f json features/\" --working-dir cucumber-example/",
      "interval": 60,
      "subscribers": [ "cucumber" ]
    }
  }
}
```


## Installation

Add the public key (if you haven’t already) as a trusted certificate

```
gem cert --add <(curl -Ls https://raw.githubusercontent.com/sensu-plugins/sensu-plugins.github.io/master/certs/sensu-plugins.pem)
gem install sensu-plugins-cucumber -P MediumSecurity
```

You can also download the key from /certs/ within each repository.

#### Rubygems

`gem install sensu-plugins-cucumber`

#### Bundler

Add *sensu-plugins-cucumber* to your Gemfile and run `bundle install` or `bundle update`

#### Chef

Using the Sensu **sensu_gem** LWRP
```
sensu_gem 'sensu-plugins-cucumber' do
  options('--prerelease')
  version '0.0.1'
end
```

Using the Chef **gem_package** resource
```
gem_package 'sensu-plugins-cucumber' do
  options('--prerelease')
  version '0.0.1'
end
```

## Notes

Sensu check that executes Cucumber tests

The check supports:
* cucumber-js
* cucumber-jvm
* Ruby Cucumber
* parallel-cucumber-js
