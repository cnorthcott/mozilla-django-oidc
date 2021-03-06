========
Settings
========

This document describes the Django settings that can be used to customize the configuration
of ``mozilla-django-oidc``.

.. attribute:: SITE_URL

   :default: No default

   URL that users access your site from. Make sure that you provide the protocol, domain,
   path and port if needed (e.g. ``<protocol>://<domain>:<port>/<path>``)

   .. note::
      This does not have to be a publicly accessible URL, so local URLs
      like ``http://localhost:8000`` or ``http://127.0.0.1`` are acceptable as
      long as they match what you are using to access your site.


.. attribute:: OIDC_OP_AUTHORIZATION_ENDPOINT

   :default: No default

   URL of your OpenID Connect provider authorization endpoint.

.. attribute:: OIDC_OP_TOKEN_ENDPOINT

   :default: No default

   URL of your OpenID Connect provider token endpoint

.. attribute:: OIDC_OP_USER_ENDPOINT

   :default: No default

   URL of your OpenID Connect provider userinfo endpoint

.. attribute:: OIDC_RP_CLIENT_ID

   :default: No default

   OpenID Connect client ID provided by your OP

.. attribute:: OIDC_RP_CLIENT_SECRET

   :default: No default

   OpenID Connect client secret provided by your OP

.. attribute:: OIDC_RP_CLIENT_SECRET_ENCODED

   :default: ``False``

   Controls whether your client secret requires base64 decoding for verification

.. attribute:: OIDC_VERIFY_JWT

   :default: ``True``

   Controls whether the OpenID Connect client verifies the signature of the JWT tokens

.. attribute:: OIDC_USE_NONCE

   :default: ``True``

   Controls whether the OpenID Connect client uses nonce verification

.. attribute:: OIDC_VERIFY_SSL

   :default: ``True``

   Controls whether the OpenID Connect client verifies the SSL certificate of the OP responses

.. attribute:: OIDC_CREATE_USER

   :default: ``True``

   Enables or disables automatic user creation during authentication

.. attribute:: OIDC_STATE_SIZE

   :default: ``32``

   Sets the length of the random string used for OpenID Connect state verification

.. attribute:: OIDC_NONCE_SIZE

   :default: ``32``

   Sets the length of the random string used for OpenID Connect nonce verification

.. attribute:: OIDC_REDIRECT_FIELD_NAME

   :default: ``next``

   Sets the GET parameter that is being used to define the redirect URL after succesful authentication

.. attribute:: OIDC_CALLBACK_CLASS

   :default: ``mozilla_django_oidc.views.OIDCAuthenticationCallbackView``

   Allows you to substitute a custom class-based view to be used as OpenID Connect
   callback URL.

   .. note::

      When using a custom callback view, it is generally a good idea to subclass the
      default ``OIDCAuthenticationCallbackView`` and override the methods you want to change.

.. attribute:: LOGIN_REDIRECT_URL

    :default: ``/accounts/profile``

    Path to redirect to on successful login. If you don't specify this, the
    default Django value will be used.

.. attribute:: LOGIN_REDIRECT_URL_FAILURE

    :default: ``/``

    Path to redirect to on an unsuccessful login attempt.


.. attribute:: LOGOUT_REDIRECT_URL

   :default: ``/``

   Path to redirect to on logout.
