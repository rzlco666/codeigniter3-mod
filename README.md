# codeigniter-mod

This is my initial setup to start a project with Codeigniter 3.

**CodeIgniter Version:** 3.1.11

## Configuration

In the `application/config/ci_seo.php` file you will find an array of configuration variables. See the following table for the usefulness of each in the library:

| Key               | Type    | Description                                                                    |
|-------------------|---------|--------------------------------------------------------------------------------|
| canonical\_url    | string  | Canonical URL of the application, which may be the result of `base\_url \(\)`  |
| site\_title       | string  | Site Title                                                                     |
| site\_description | string  | Website Description                                                            |
| site\_image       | string  | Illustrative site image \(size is usually 1200x630\)                           |
| twitter\_user     | string  | Twitter username including @                                                   |
| fb\_app\_id       | integer | Facebook app ID with which the site is associated \(developer\.facebook\.com\) |
| fb\_page\_id      | integer | Facebook Page ID with which the site is associated                             |

## How to use

After performing the installation and configuration, just call the method `$this->ci_seo->add_tags()` informing the parameters corresponding to the title, description and illustrative image of the page.

```
$this->ci_seo->add_tags('Page title', 'Page Description', 'image/path');
```

The `$this->ci_seo->add_tags()` method can be called either directly inside the `<head> </head>` tag or inside some method in the controller, returning the data to a variable that should be passed to the view should be retrieved inside `<head> </head>`.

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8">
    <?= $this->ci_seo->add_tags('Page title', 'Page Description', 'image/path'); ?>
</head>
<body></body>
</html>
```

## Special Thanks

[jlamim][1] for [SEO optimization library][2]

[1]: https://github.com/jlamim
[2]: https://github.com/jlamim/ci-seo
