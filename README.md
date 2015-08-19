[![Latest Stable Version](https://poser.pugx.org/sebastian/money-intl-formatter/v/stable.png)](https://packagist.org/packages/sebastian/money-intl-formatter)

# Money IntlFormatter

Implementation of `SebastianBergmann\Money\Formatter` that uses PHP's built-in NumberFormatter.

## Installation

Simply add a dependency on `sebastian/money-intl-formatter` to your project's `composer.json` file if you use [Composer](http://getcomposer.org/) to manage the dependencies of your project.

Here is a minimal example of a `composer.json` file:

    {
        "require": {
            "sebastian/money-intl-formatter": "~1.0"
        }
    }

## Usage Examples

#### Formatting a Money object using PHP's built-in NumberFormatter

```php
use SebastianBergmann\Money\Currency;
use SebastianBergmann\Money\Money;
use SebastianBergmann\Money\IntlFormatter;

// Create Money object that represents 1 EUR
$m = new Money(100, new Currency('EUR'));

// Format a Money object using PHP's built-in NumberFormatter (German locale)
$f = IntlFormatter::fromLocale('de_DE');

print $f->format($m);
```

The code above produces the output shown below:

    1,00 €

