jquery.mentionsInput (dtime flavor)
=================

This is a modified version of: http://podio.github.com/jquery-mentions-input

with the following changes:

* Adds onCaret support (enabled by default)
* The text inside the textarea will be used and properly initialized if the
  textarea already has a value
* Multiple trigger characters are allowed - set triggerChar to an array. We use
  ['@','#'] so that tag mentions are treated the same way as username mentions.
  It is your job to filter by trigger character in the `onDataRequest` function
  (which takes a fourth argument `trigger`).
* The trigger character is included in the value of the mention so you can
  still see it. This is useful for distinguishing between multiple trigger
  chars. This only happens if a trigger is set on the mention, or a default
  trigger char is set.
* Formatting now is of the form:

  `[@username](user:user_id)` instead of `@[username](user:user_id)`

