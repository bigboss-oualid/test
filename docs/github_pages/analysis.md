# Analysis

[Back to summary](../index.md)

Respect [PSR-1](https://www.php-fig.org/psr/psr-1) & [PSR-12](https://www.php-fig.org/psr/psr-12).
## Launch analysis

The below commands will analyze the code in the ``src`` folder of the project & generate html output :

PHP Mess Detector:
```shell
.\vendor\bin\phpmd .\src\ html .\phpmdRules.xml > .\analyzes\LTS\backend\messDetector\phpMDReport.html
```

PSalm:
```shell
vendor/bin/psalm  --show-info=true --output-format=xml | xsltproc vendor/roave/psalm-html-output/psalm-html-output.xsl - > .\analyzes\LTS\backend\psalm\psalm-report.html
```

PHPStan:
```shell
./vendor/bin/phpstan analyse -c phpstan.neon --error-format fileoutput
```

PHPMetrics:
```shell
./vendor/bin/phpmetrics --config=phpMetricsConfig.json
```

## Fix errors
Use ``PHP Code Sniffer`` to fix some errors automatically :
```
vendor/bin/phpcbf
```