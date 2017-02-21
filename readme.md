# Kirby Starthook

*Version 0.1*

With the starthook you will have access to the page object directly from your `config.php` file.

You can pass global data to your templates and snippets.

You can also do redirects on certain conditions.

**[How to install Kirby Starthook](docs/install.md)**

## Usage

Put your starthook code into the `config.php` file.

### Example 1

**Pass global data to templates and snippets**

The data that is returned here can later be used in all your templates and snippets:

```php
kirby()->hook('starthook', function($page) {
  starthook::return(array(
    'foo' => 'my first template variable',
    'bar' => 'my second template variable'
  ));
});
```

### Example 2

**Redirect on condition**

On a condition, redirect to another page.

```php
kirby()->hook('starthook', function($page) {
  if($page->title() == 'Project A') {
    go(page('projects'), 301);
  }
});
```

## Changelog

**0.1**

- Initial release

## Requirements

- [**Kirby**](https://getkirby.com/) 2.4.1+

## Disclaimer

This plugin is provided "as is" with no guarantee. Use it at your own risk and always test it yourself before using it in a production environment. If you find any issues, please [create a new issue](https://github.com/jenstornell/kirby-starthook/issues/new).

## License

[MIT](https://opensource.org/licenses/MIT)

It is discouraged to use this plugin in any project that promotes racism, sexism, homophobia, animal abuse, violence or any other form of hate speech.

## Credits

- [Jens Törnell](https://github.com/jenstornell)