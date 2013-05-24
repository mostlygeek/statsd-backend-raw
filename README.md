Simple backend for statsd that just dumps the data it sends in 
a `flush` event to the console.

## Installation

Add this to your `package.json` in dependencies

    "dependencies": {
        ....
        "statsd-backend-raw": "git://github.com/mostlygeek/statsd-backend-raw.git"
    }

Then in your StatsD configuration add `statsd-backend-raw` to the `backends` key:

    {
      port: 8125
    , debug: true
    , backends: [ "statsd-backend-raw" ]
    , flushInterval : 2500
    , console: {
        prettyPrint: true
      }
    };

