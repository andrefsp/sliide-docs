.. partners documentation master file, created by
   sphinx-quickstart on Mon Apr 10 11:59:59 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Sliide SDK documentation!
====================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:


Sliide SDK provides an easy way to integrate with any app so that it can provide Ad Funded features within your app. This documentation will show how to integrate Sliide SDK with any app.


Introduction
------------

Sliide SDK provides a way for any app to build user credit ad funds. These funds can than be used to fund any payed app feature.  

The SDK is designed in a way that makes it very simple to start using Sliide as it virtually does not require any user registration. The SDK simply starts and builds credit for a particular user specified by unique identifier ``user_id`` and also a ``app_id``. We will be exploring this later on.

The step required is the app registeration.The app registration process will provide an ``app_id`` and an ``app_secret``. There two valus will help Sliide to know what application does a user belong to.  


The next block shows an high level overview of credit build-up.

.. code:: java
                        
    +-------------------+                                               
    |    App            |                                               
    |   +---------------+                  +---------------+
    |   | SDK(Sliide)   |   <------------> |  Sliide API   |
    |   |   * App-Id    |      User-Id     +---------------+
    |   |   * User ID   |      App-Id
    +---+---------------+



When a certain level of credit is reached, a user can than request to cashout its credits to the App. This process is based on the App to provide a Server-To-Server URL so that Sliide can inform the app server of the user intentions to cashout. This process is fully managed by Sliide . 

The block shows an overview. 


.. code:: java
                        
    +-------------------+                                               
    |    App            |                                               
    |   +---------------+                   +---------------+                +---------------+
    |   | SDK(Sliide)   |   <-------------> |  Sliide API   | <------------> |   App Server  |
    |   |   * App-Id    |       User-Id     +---------------+    User-Id     +---------------+
    |   |   * User ID   |       App-Id                           Amount
    +---+---------------+       Amount




Along this document we will be explaining app registration and cashout integration which is the only two needed integrations.



Application Registration
========================



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
