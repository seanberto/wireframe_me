NOTE: This module is nothing yet - in fact, it doesn't work.

But per a designer's suggestion, I've started building a module that will let Drupal front-end UI designers quickly pencil out "clickable" Drupal wireframes.

The idea is really simple. The module comes with a simple configuration file in which a designer can list all the wireframed pages they need with the following format:

wireframe[path] = the URL you want to hang the wireframe on
wireframe[title] = The page title
wireframe[content] = whatever markup you want on the page .

Three awesome points to this:

* You can hang blocks on these paths using contexts and boxes - and that work is permanent. In other words, you might kill the wireframed page, but if the path still exists, any context you've created for the path live on.

* I'm going to set the "weight" of this module really low, which means that if once module (or you) creates a page callback with the same URL, the wireframe goes away gracefully.

* Since you can put whatever you want in the body of the page callback, you could really easily embed a Flickr wireframe.