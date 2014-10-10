Lorem ipsum generator for the Laravel Framework
====================================================================


This service provider uses the [loripsum.net](http://loripsum.net/) API for text generation via the [magyarjeti/loripsum-client](https://github.com/magyarjeti/loripsum-client) library.

## Installation

### Manually

Add this to your composer.json:

```json
{
    "require": {
        "magyarjeti/laravel-lipsum": "dev-master"
    }
}
```

Then run:

```bash
php composer.phar update
```

### CLI only

```bash
php composer.phar require magyarjeti/laravel-mongo dev-master
```

## Setup

Append service provider to your provider in `app/config/app.php`:

```php
'providers' => array(
    // ...
    'Magyarjeti\LaravelLipsum\LipsumServiceProvider',
)
```

Optionally register an alias at the same place:

```php
'aliases' => array(
    // ...
    'Lipsum' => 'Magyarjeti\LaravelLipsum\LipsumFacade',
)
```

## Usage

Generate HTML text:

```php
Lipsum::html();
```

Generate five paragraph HTML text with headers, link and unordered list:

```php
Lipsum::headers()->link()->ul()->html(5);
```

Generate three short plain text paragraphs:

```php
Lipsum::short()->text(3);
```

### More text formatting options

- **short, medium, long, verylong** - The average length of a paragraph.
- **decorate** - Add bold, italic and marked text.
- **link** - Add links.
- **ul** - Add unordered lists.
- **ol** - Add numbered lists.
- **dl** - Add description lists.
- **bq** - Add blockquotes.
- **code** - Add code samples.
- **headers** - Add headers.
- **allcaps** - Use ALL CAPS.
- **prude** - Prude version.

## Author

Magyar Jeti Zrt.

## License

This package  is licensed under the MIT License - see the ```LICENSE``` file for details!
