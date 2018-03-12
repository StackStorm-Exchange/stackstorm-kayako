# Kayako Integration Pack

This pack provides actions for integation with the [Kayako](https://www.kayako.com) customer ticket management system.

## Configuration

Copy the example configuration in [kayako.yaml.example](./kayako.yaml.example)
to `/opt/stackstorm/configs/kayako.yaml` and edit as required.

It must contain:

* ``url`` - URL for your Kayako API, e.g. https://kayako.example.com/api/index.php
* ``api_key`` - An API token generated in the admin interface
* ``secret_key`` - Secret key used for signature

To obtain API and Secret keys, see the docs [here](https://kayako.atlassian.net/wiki/spaces/DEV/pages/4817002/Kayako+REST+API#KayakoRESTAPI-Authentication)

You can also use dynamic values from the datastore. See the
[docs](https://docs.stackstorm.com/reference/pack_configs.html) for more info.

**Note** : When modifying the configuration in `/opt/stackstorm/configs/` please
           remember to tell StackStorm to load these new values by running
           `st2ctl reload --register-configs`

## Actions

* ``create_ticket`` - Creates a new ticket with the given subject and description.
* ``create_ticket_post`` - Adds a post to a ticket
