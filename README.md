phphighcharts-exporter
======================

PHP wrapper for exporting Highcharts created with PhpHighCharts with PhantomJS.

Authors
-------

* Bart Huttinga <barthuttinga@gmail.com>

Requirements
------------

* [Highcharts](http://www.highcharts.com/)
* [PhantomJS](http://phantomjs.org/)
* [PhpHighCharts](https://github.com/barthuttinga/phphighcharts)

Installation
------------

 1. Add the library to composer.json:

```
// composer.json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/barthuttinga/phphighcharts-exporter"
        }
    ],
    "require":{
        "barthuttinga/phphighcharts-exporter": "dev-master"
    }
}
```

 2. Use Composer to download and install the library:

```
$ php composer.phar update barthuttinga/phphighcharts-exporter
```

Usage
-----

Export a chart:

```
$chart = new PhpHighCharts\HighChart();
// build chart...

$phantomJsBinary  = '/path/to/phantomjs';
$conversionScript = '/pah/to/highcharts/exporting-server/phantomjs/highcharts-convert.js';
$cacheDir         = '/path/to/cachedir';

$exporter = new Exporter($phantomJsBinary, $conversionScript, $cacheDir);
$file = $exporter->export($chart);
```

Reporting an issue or a feature request
---------------------------------------

Issues and feature requests are tracked in the [GitHub issue tracker](https://github.com/barthuttinga/phphighcharts-exporter/issues).
