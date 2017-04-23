qooxdoo Dialog widgets
======================

see http://cboulanger.github.io/qx-contrib-Dialog/

A set of often used dialog widgets for the qooxdoo framework.

- Alert
- Confirm
- Form
- Login
- Prompt
- Select
- Wizard
- Progress

Demo: http://cboulanger.github.io/qx-contrib-Dialog/build/index.html

API Viewer: http://cboulanger.github.io/qx-contrib-Dialog/api/index.html#dialog

See demo/default/source/class/dialog/demo/Application.js for examples how to use
the widgets.

Installation:
-------------
- Download and extract ZIP to a folder in your project
- in your qooxdoo project's config.json "jobs"/"libraries"/"library" section, add
  ```
  {
    "manifest": "path/to/qx-contrib-Dialog/Manifest.json"
  }
  ```

Changelog
----------

v1.3
- Bumped qooxdoo version to 5.1
- Merged changes from jbruwes/qooxdialog
  - replaced base widget qx.ui.GroupBox with modal qx.ui.window.Window
  - new black and white SVG icons
- Added caption parameter to shorthand methods.
- Since a modal window has its own blocker, the  default coloured blocker has
  been removed. If you want the old behavior, call `dialog.Dialog.useBlocker(true)`.
- Prettified with the default settings of https://github.com/prettier/prettier
- Progress Widge enhancements:
  - added 'hideWhenCancelled' property (default: true) to allow "cleanup" or
    similar actions to be displayed after the cancel button has been pressed.
- Added 'cancelOnEscape' property (default: false) which triggers the 'cancel'
  button action if the user presses the Escape key and 'allowCancel' is true.

v1.2
- fixed a bug that prevented submitting the login dialog by pressing enter
  (patch by @novij)
- added "Forgot Password?" button to login widget

v1.1
- compatible with qooxdoo v4.0
- Progress dialog widget added

v1.0
- compatible with qooxdoo v3.5

TODO
----
- Tab and focus handling is still buggy: Users can tab into non-modal widgets.
- Rewrite using child controls, to make dialogs truly themeable.
