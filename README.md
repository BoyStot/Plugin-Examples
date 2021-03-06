# OctoPrint Plugin Examples

This repository collects the sources of examples for writing plugins for [OctoPrint](https://octoprint.org).

Currently the following example plugins and more can be found here:

  * **add_tornado_route**: Single file plugin (place it in ``~/.octoprint/plugins``) that shows how to utilize the
    [octoprint.server.http.routes](http://docs.octoprint.org/en/master/plugins/hooks.html#octoprint-server-http-routes) hook
    to add additional routes with custom ``RequestHandlers`` to the server configuration.
  * **custom_action_command**: Single file plugin (place it in ``~/.octoprint/plugins``) that shows how to utilize the
    [octoprint.comm.protocol.action hook](http://docs.octoprint.org/en/master/plugins/hooks.html#octoprint-comm-protocol-action)
    hook and how to register hook handlers that are part of a mixin implementation. The plugin will listen for 
    firmware messages of the form ``// action:custom`` and if received will log that it received the "custom" action
    from the firmware.
  * **custom_template_consumer**: Single directory plugin (place it in ``~/.octoprint/plugins``) that shows how to
    have a plugin inject itself into custom places provided through other plugins in the web interface through utilizing
    a custom template type if the presence of the provider of that template is detected.
  * **custom_template_provider**: Single directory plugin (place it in ``~/.octoprint/plugins``) that shows how to
    provide a custom template type through the [octoprint.ui.web.templatetypes hook](http://docs.octoprint.org/en/master/plugins/hooks.html#octoprint-ui-web-templatetypes)
    and how to display templates of that type.
  * **helloworld**: A simple plugin that injects itself into various places in OctoPrint's web interface to display
    "Hello World". Shows the basic structure of a plugin, how plugins can execute code at startup, inject themselves into
    the interface and how they can control when their content is shown based on internal state of the UI such as login
    information.
  * **increase_bodysize**: Single file plugin (place it in ``~/.octoprint/plugins``) that shows how to increase the 
    maximum allowed request body size for specific endpoints by utilizing the 
    [octoprint.server.http.bodysize hook](http://docs.octoprint.org/en/master/plugins/hooks.html#octoprint-server-http-bodysize).
  * **message_on_connect**: Single file plugin (place it in ``~/.octoprint/plugins``) that shows how to utilize the
    [octoprint.comm.protocol.scripts hook](http://docs.octoprint.org/en/master/plugins/hooks.html#octoprint-comm-protocol-scripts)
    by adding an ``M117 OctoPrint connected`` to the GCODE script sent to the printer after OctoPrint connected to
    it.
  * **rewrite_m107**: Single file plugin (place it in ``~/.octoprint/plugins``) that shows how to utilize the
    [octoprint.comm.protocol.gcode hook](http://docs.octoprint.org/en/master/plugins/hooks.html#octoprint-comm-protocol-gcode)
    by swapping the (deprecated) ``M107`` command with the equivalent ``M106 S0``.
  * **strip_all_comments**: Single file plugin (place it in ``~/.octoprint/plugins``) that shows how to utilize the
    [octoprint.filemanager.preprocessor hook](http://docs.octoprint.org/en/master/plugins/hooks.html#octoprint-filemanager-preprocessor)
    by removing the comments (and empty lines) from all uploaded/generated GCODE files ending on the name postfix "_strip".

## Further Links

  * [OctoPrint](https://octoprint.org)
  * [OctoPrint Source Repository](https://github.com/foosel/OctoPrint)
  * [OctoPrint Plugin Documentation](http://docs.octoprint.org/en/master/plugins/index.html)
  
## License

These examples are licensed under the MIT license. See also `LICENSE` in the source folder.
