# sfSmartContextPlugin

[![StyleCI](https://github.styleci.io/repos/49590448/shield?branch=master)](https://github.styleci.io/repos/49590448)

symfony 1.x plugin to add [SmartContext](http://www.smartcontext.pl/) integration.

## Instalation

  * Install the plugin:

    ~~~sh
    composer require tomasz-rup/sf-smartcontext-plugin
    ~~~

  * Add the sfSmartContextFilter to your filter chain:

    ~~~yaml
    rendering: ~
    security:  ~

    # insert your own filters here
    smart_context:
      class: sfSmartContextFilter

    cache:     ~
    common:    ~
    execution: ~
    ~~~

## Configuration

  * Global configuration

    Global configuration is done in your application's app.yml file:

    ~~~yaml
    all:
      smart_context_plugin:
        site:    http__yoursite.com
        enabled: true
    ~~~

  * Configuration per module

    To disable SmartContext in action **index** in module **default** add to your  ``apps/frontend/modules/default/config/module.yml`` file following configuration:

    ~~~yaml
    all:
      index:
        smart_context:
          enabled: false
    ~~~
