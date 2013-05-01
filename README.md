# CodebaseHQ

This is a [Laravel Package](http://laravel.com/) that makes it easy to integrate with [Codebase](http://www.codebasehq.com/) features.  Currently, this means pushing exceptions to [Codebase's Exception](http://blog.atechmedia.com/2012/08/exception-tracking-in-codebase/) tracker but I'd like to add more features if people have suggestions.

## Installation

1. Install it with `php artisan bundle:install laravel-plus-codebase` 
2. Register the bundle in application/bundles.php with: `return array('laravel-plus-codebase' => array('auto' => true))`

## Configuration

* Add the API key for your Codebase project to bundles/laravel-plus-codebase/config/codebase.php.  You can get this by visiting the Exceptions view of a Codebase project, you'll see it displayed on the page.  It looks something like "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

## Usage

If you have logging turned on (the config directive "error.log" in application/config/error.php), all of your exceptions will now be automatically be posted to the Exceptions view in your Codebase project.  Note: error logs will NOT be generated in your filesystem, only on Codebase.

By default, your "local" enviornment will not post exceptions to Codebase.  This can be changed in the bundles config/local/codebase.php file.
