---
title: Papi docs

language_tabs:
  - php

toc_footers:
  - <a href='http://github.com/wp-papi/papi'>Fork me on GitHub</a>
  - <a href='http://wp-papi.github.io/'>Papi project site</a>
  - <a href='apigen/'>API reference docs</a>
  - <a href='https://github.com/wp-papi/papi/releases'>Changelog</a>
  - <a href='https://wp-papi.github.io/docs-1.x'>Documentation for Papi 1.x</a>

includes:
  - upgrade_guide
  - page_type_directory
  - actions
  - api
  - api_field
  - api_page
  - api_option
  - box
  - porter
  - option_type
  - page_type
  - properties
  - property_filters
  - conditional_logic
  - setting_filters
  - custom_property

search: true
---

# Introduction

**This is the documentation for Papi 2.x**

[**Go to documentation for Papi 1.x**](https://wp-papi.github.io/docs-1.x)

Papi has a different approach on how to work with fields and page types in WordPress. The idea is coming from how Page Type Builder in EPiServer works and has been loved by the developers.

So we though why don't use the same approach in WordPress? Papi is  running in production and has been easy to work with when it came to add new fields. Papi don't have any admin user interface where you should add fields, we use classes in PHP, where one class represents one page type and in your class you add all fields you need. It's that easy!

Papi does not save the property type value in the database, only the value of the property is saved since the type value exists in the page type file.

Papi is completely open-source. If you want to help with its development you can submit your suggestions or improvements on in the [Github repository](https://github.com/wp-papi/papi).

## Requirements

* WordPress >= 4.0
* PHP >= 5.4.7

## Installation

If you're using Composer to manage WordPress, add Papi to your project's dependencies. Run:

`composer require wp-papi/papi`

Or manually add it to your `composer.json`:

```json
{
  "require": {
    "php": ">=5.4.7",
    "wordpress": "~4.2",
    "wp-papi/papi": "~2.0"
  }
}
```
