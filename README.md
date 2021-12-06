# Start Digital WordPress Helpers

## What is this repository?

This is a collection of helpful functions and classes for use when developing WordPress websites.

### Helpers

1. [Simple Custom Post Type API](#CustomPostType)

### CustomPostType

The simplest use case is to create a new instance of the class with the name of your post type:

```
$books = new CustomPostType('Books');
```

The API offers two methods for updating both labels and arguments, `set_labels()` and `set_args()`. Both take an array of the either the labels or arguments for the `register_post_type()` function ([see accepted parameters here](https://developer.wordpress.org/reference/functions/register_post_type/#parameter-detail-information)).

For example, we could set the override the default singular name if it doesn't make sense:

```
$people = new CustomPostType('People');
echo $people['labels']['singular_name'] // People

$people->set_labels(['singular_name' => 'Person]);
echo $people['labels']['singular_name'] // Person
```
