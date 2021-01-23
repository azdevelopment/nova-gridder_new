# Nova Gridder

This package allows customize your resource details using grid and class systems.

## Example

![Example](https://github.com/demency/nova-gridder/blob/master/example.png)

## Requirements

This package requires:

- PHP ^7.3|^8.0.*.
- Laravel Nova ^2.0 or ^3.0.

##  Installation

You can install this package in a Laravel app that uses Nova via composer:

```
composer require alizada/nova-gridder
```

## Usage

Add the following code in your own resource implementation:

```php
<?php

...

class YourResource extends Resource {

    ...

    public function fields(Request $request)
    {
        return [
            ...

            // Are you ready?
            // --------------
            // 1. Use gridder method
            // 2. Set options for rendering
            // 3. See the results
            Field::make(__('Column'), 'column') // Use whatever Field
                ->gridder([
                    'labelSize' => 'w-full',
                    'contentSize' => 'w-full',
                    'panelSize' => 'w-1/5', // Use field as box in a Panel
                    'additionalLabelClasses' => 'text-center',
                    'additionalContentClasses' => 'text-center py-2',
                    'additionalPanelClasses' => '', // This remove the border-bottom per field
                ])
        ];
    }
```

## Changelog

### 1.0.1

- Now support nova 3.0.
- Some wrong type fixed.

### 1.0.0

- Recently published.

## Disclaimer

This package isn't tested. Feel free to make PR with improvements.


