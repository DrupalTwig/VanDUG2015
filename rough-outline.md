
Problem -> Solution


# Pipeline (JP)

D7 Pipeline vs D8 Pipeline
(process is gone and everything is in a template)

# Filename changes: (LW)

```THEME.info
THEME.info.yml

template.php
THEME.theme

TEMPLATE.tpl.php
TEMPLATE.html.twig

theme-settings.php (SAME)
```

# Info (LW)
```THEME.info
THEME.info.yml
```
# base themes (JP)
(stable vs classy) vs (bartik vs seven) vs stark vs core (aka false, aka wild west)
```
base theme: false (core)  < stark
base theme: stable (default)
base theme: classy (this is if you want drupal classes and markup)
```

# Templates (JP)
```
TEMPLATE.tpl.php
TEMPLATE.html.twig
```

# Theme function & template changes (JP)
```
D7         D8
theme_* -> *.html.twig
THEME_status_messages() -> status-messages.html.twig

D7              D8
node.tpl.php -> node.html.twig
```

# Twig Syntax (LW)
print drupal_render() -> {{ }}
<?php if (!empty($var)) : ?> -> {% if var %}
<?php /* */ ?> -> {# comment #}


# Twig Magic (JP)
Simplified - more detail go to source code!

# Attirbutes (JP)

The variables before and the Attribute class now.

# MOAR BLOCKS (LW)
```
branding block
system messages block
menu block
```



# Preprocess (LW)
DIDN'T CHANGE, still get up there (except doesn't have suggestions...)

# Suggestions (LW)
```
D7
in your THEME_prepreprocess_HOOK
$variables['theme_hook_suggestions'][] = 'page__peanuts';

D8
HOOK_theme_suggestions_HOOK
mymodule_theme_suggestions_block(array $variables) (only works in MODULES)
HOOK_theme_suggestions_HOOK_alter()
THEME_theme_suggestions_block(array &$suggestions, array $variables) (only works in MODULES or THEME).
```

# Libraries (JS/CSS assets) (LW)

```
THEME.libraries.yml
{{ attach_library('classy/node') }}

drupal_add_js()
drupal_add_css() don't exist
https://www.drupal.org/node/2169605
https://www.drupal.org/node/2379475
```

# SMACCS

# BEM/CEM

# Attachements (JP)
```
D7
    hook_page_build()
    hook_page_alter()

D8
    hook_page_attachments()
    hook_page_attachments_alter()
    hook_page_top()
    hook_page_bottom()
```

https://www.drupal.org/node/2357755

@TODO needs examples.

D7
$render_array = array('#attached' => array());

On preprocess Only in D8
 $variables['#attached']
And on all render arrays like D7

# Debug Tools(JP)

D7              D8
theme_debug -> twig.debug
local.settings.php
twig.debug
Example output.

# ¿QUESTIONS?
