# Upgrade guide

## Upgrade to 2.x from 1.x

Change `wp-papi/papi` version to `~2.0` in your `composer.json` file and run `composer update`.

### API

`papi_fields` is deprecated and replaced with `papi_get_slugs`.

### API Field

`papi_field` is deprecated and replaced with `papi_get_field` because the name can be confusing when `papi_update_field` and `papi_delete_field` exists.

It will still work to use `papi_field` but you will get a deprecated warning.

### API Page

`current_page` is deprecated. You can use `papi_get_page` with no argument to get the same result.

It will still work to use `current_page` but you will get a deprecated warning.

### Properties

#### Dropdown and Post property

In 2.0.0 `placeholder` setting replaced `blank_text` and `include_blank`.


#### Relationship property

In 2.0.0 `choose_max` was renamed to `limit`.

### Settings filters

#### Show standard page type for post type

The filter `papi/settings/standard_page_type_{$post_type}` was renamed to `papi/settings/show_standard_page_type_{$post_type}`.
