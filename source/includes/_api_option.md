# API Option

## papi_delete_option

```php
<?php

/**
 * Example of `papi_delete_option` function.
 */

$success = papi_delete_field( 'twitter_url' );
```

### Description

With this function you can delete property value from the database. It will return false if can't update or find the property in a option type.

### Parameters

Parameter | Default | Required |
----------|---------|----------|------------------------------------------------
$slug     |         | yes      | The property slug to delete value from

## papi_get_option

```php
<?php

/**
 * Example of `papi_get_option` function.
 */

echo papi_get_option( 'twitter_url' );

// with default value
echo papi_get_option( 'twitter_url', 'http://twitter.com/frozzare' );
```

### Description

Fetch property value from option type.

You can also use [the_papi_option](#the_papi_option) to display it without `echo`

### Parameters

Parameter | Default | Required | Description
----------|---------|----------|------------------------------------------------
$slug     |         | yes      | The property slug to fetch value from
$default  | null    | no       | When a default value is passed as argument it will use that value as return value and echo it if the property value is empty or don't exists

## papi_update_option

```php
<?php

/**
 * Example of `papi_update_option` function.
 */

$success = papi_update_option( 'twitter_url', 'http://twitter.com/frozzare' );
```

### Description

With this function you can update property value from the database. It will return false if can't update or find the property in a option type.

### Parameters

Parameter | Default | Required |
----------|---------|----------|------------------------------------------------
$slug     |         | yes      | The property slug to update property value

## the_papi_option

```php
<?php

/**
 * Example of `the_papi_option` function.
 */

the_papi_option( 'twitter_url' )

// with default value
the_papi_option( 'twitter_url', 'http://twitter.com/frozzare' );
```

### Description

This function will echo the value of a property using the property slug.

You can also use [papi_option](#papi_option) to fetch the value into a variable.

### Parameters

Parameter | Default | Required | Description
----------|---------|----------|------------------------------------------------
$slug     |         | yes      | The property slug to fetch value from
$default  | null    | no       | When a default value is passed as argument it will use that value as return value and echo it if the property value is empty or don't exists
