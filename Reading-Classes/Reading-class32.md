# API Reference

### GenericAPIView

Each of the concrete generic views provided is built by combining GenericAPIView, with one or more mixin classes.

### Attributes

- Basic settings:

The following attributes control the basic view behavior.

queryset - The queryset that should be used for returning objects from this view. Typically, you must either set this
attribute, or override the get_queryset() method. If you are overriding a view method, it is important that you call
get_queryset() instead of accessing this property directly, as queryset will get evaluated once, and those results will
be cached for all subsequent requests.
serializer_class - The serializer class that should be used for validating and deserializing input, and for serializing
output. Typically, you must either set this attribute, or override the get_serializer_class() method.
lookup_field - The model field that should be used to for performing object lookup of individual model instances.
Defaults to 'pk'. Note that when using hyperlinked APIs you'll need to ensure that both the API views and the serializer
classes set the lookup fields if you need to use a custom value.
lookup_url_kwarg - The URL keyword argument that should be used for object lookup. The URL conf should include a keyword
argument corresponding to this value. If unset this defaults to using the same value as lookup_field.

- Pagination:

The following attributes are used to control pagination when used with list views.

pagination_class - The pagination class that should be used when paginating list results. Defaults to the same value as
the DEFAULT_PAGINATION_CLASS setting, which is 'rest_framework.pagination.PageNumberPagination'. Setting
pagination_class=None will disable pagination on this view.

- Filtering:

filter_backends - A list of filter backend classes that should be used for filtering the queryset. Defaults to the same
value as the DEFAULT_FILTER_BACKENDS setting.