## Sensu-Plugins-cucumber

[ ![Build Status](https://travis-ci.org/sensu-plugins/sensu-plugins-cucumber.svg?branch=master)](https://travis-ci.org/sensu-plugins/sensu-plugins-cucumber)
[![Gem Version](https://badge.fury.io/rb/sensu-plugins-cucumber.svg)](http://badge.fury.io/rb/sensu-plugins-cucumber)
[![Code Climate](https://codeclimate.com/github/sensu-plugins/sensu-plugins-cucumber/badges/gpa.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-cucumber)
[![Test Coverage](https://codeclimate.com/github/sensu-plugins/sensu-plugins-cucumber/badges/coverage.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-cucumber)
[![Dependency Status](https://gemnasium.com/sensu-plugins/sensu-plugins-cucumber.svg)](https://gemnasium.com/sensu-plugins/sensu-plugins-cucumber)

## Functionality

## Files
 * bin/check-cucumber.rb

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

[Installation and Setup](http://sensu-plugins.io/docs/installation_instructions.html)

## Notes

Sensu check that executes Cucumber tests

The check supports:
* cucumber-js
* cucumber-jvm
* Ruby Cucumber
* parallel-cucumber-js
