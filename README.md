# NAME

Template::Plugin::StripComments - Template Toolkit filter to strip comment blocks

# SYNOPSIS

```
[% USE StripComments %]
...
[% FILTER stripcomments %]
  /* C-style block comments get removed */

  <!-- as do HTML comments -->
[% END %]
...
[% text | stripcomments %]
```

# DESCRIPTION

`Template::Plugin::StripComments` is a filter plugin for [Template::Toolkit](https://metacpan.org/pod/Template%3A%3AToolkit),
which strips comment blocks from the filtered text.

The following types of comment blocks are stripped:

- /\* c-style comments \*/
- &lt;!-- HTML comments -->

# METHODS

- init()

    Initializes the template plugin.

- filter($text)

    Filters the given text, removing comment blocks as necessary.

# AUTHOR

Graham TerMarsch <cpan@howlingfrog.com>

# COPYRIGHT

Copyright (C) 2007, Graham TerMarsch.  All Rights Reserved.

This is free software; you can redistribute it and/or modify it under the same
terms as Perl itself.

# SEE ALSO

[Template::Plugin::Filter](https://metacpan.org/pod/Template%3A%3APlugin%3A%3AFilter).
