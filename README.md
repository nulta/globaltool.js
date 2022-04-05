# globaltool.js
Simple Javascript utilities in a single file

## Functions
- `$q` = `document.querySelector`
- `$qAll` = `document.querySelectorAll`
- `$new(tag, {parent, attributes, classes, text, id})`
  - Creates a new element with given settings. Parameters except _tag_ is optional.
    - _`parent`_ : `HTMLElement`
    - _`attributes`, `classes`_ : `string[]`
    - _`tag`, `text`, `id`_ : `string`
- `$globalEvent(event, selector, callback, options)`
  - Creates a global event on body, which is triggered when the event target matches the given selector.
  - Like `Element.addEventListener`, but works with all elements matching the selector.

### $ajax
JSON ajax utilities using `fetch`.
- `$ajax._baseURI`
  - The base URI of your API server.
  - When a _relative path_ is recieved on `$ajax`, baseURI will be prepended on it.
- `$ajax._logToConsole`
  - When true, Every ajax request by `$ajax` will make a fancy console log.
- `$ajax.get(url, data)`
- `$ajax.post(url, data)`
- `$ajax.patch(url, data)`
- `$ajax.put(url, data)`
- `$ajax.delete(url, data)`
  - Sends request to the server. Returns a Javascript object parsed from JSON.
