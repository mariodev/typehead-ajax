typehead-ajax
=============

Improved bootstrap-typeahead.js
Bootstrap ver: 2.2.2

The main goal of improvement, is to add data-id attribute to each li tag, so that we can retrieve selected item by its id.

Example usage (ajax):
```javascript
$('.typeahead').typeahead({
  source: function(query, callback) {
    $.get('/your/route/', {q: query}, function(items) {
      callback(items);
    });
  },
  
  updater: function (item) {
    // do anything with item.id, item.value
    return item.value;
  }
});
```
