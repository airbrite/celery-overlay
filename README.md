celery-overlay
==============

This is the full source of the Celery overlay javascript file that gets loaded when embedding celery.js

## Parent Window Callbacks

Celery will check for callback methods attached to your main page.
When certain events happen in the Celery checkout process, these callback methods will be fired:

```
function onCeleryOpen() {
	console.log("Celery opened!");
}
function onCeleryClose() {
	console.log("Celery closed!");
}
function onCeleryOrderPlaced() {
	console.log("Celery placed!");
}
```

This is good place to put analytics callbacks.  For instance:

```
function onCeleryOrderPlaced() {
    ga('send', 'event', 'preorder', "complete");
}
```