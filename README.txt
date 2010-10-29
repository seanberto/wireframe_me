// Wireframe Me - A simple developer module for stubbing out wireframed pages in Drupal.
// Developed by Sean Larkin, ThinkShout.com

== About Wireframe Me ==

Front-end designers, project managers, and clients consistently ask Drupal back-end engineers for clickable wireframes early in the development cycle. When developing "agilely", this is particularly important. Unfortunately, it's not always easy to manage placeholder page content in Drupal. Often it's done by creating placeholder nodes, but that requires either maintaining database dumps containing these nodes, or creating them on the fly with install scripts.

Wireframe Me attempts to address this issue in a light-weight and codified manner by providing a simple configuration file, similar to a .info file, for creating/managing placeholder URL paths, page titles, and page body content.

Interestingly, this module leverages Drupal 7's new hook_module_implements_alter function such that the paths/pages created by this module are overridden quietly when another module, node, or view creates a path with the same URL.

Also, since really any value can be returned for the page body, you can simply embed images of mocked-up content/functionality that you've yet to implement. You can also "get started" hanging blocks on these stubbed out pages by combining this approach with the Context, Boxes, and Views modules.

== Installation/Usage ==

* Download and enable the module.
* Add stubbed out pages in ./wireframes/wireframe_me.wireframes.inc.
* Optionally, use Context, boxes and views to add permanent content to these paths.

* NOTE: B/c of the way that we're currently flushing the menu cache, you must manually flush the menu cache to see changes to the wireframed pages as an anonymous site visitor. When logged in, you have to reload the page twice to pick up changes. We're working to fix ths.

== ToDo ==

* Find and parse *.wireframes.inc files created/maintained in other modules.
* Check filter format of stubbed out pages for security.
* Rework flushing of menu cache.