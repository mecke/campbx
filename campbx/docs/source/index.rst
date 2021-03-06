======
CampBX
======

About
=====

This library provides python bindings for the `CampBX bitcoin trading platform <http://campbx.com>`_.
To obtain API access please `see the documenation at CampBX <https://campbx.com/api.php>`_.

.. note::
  
  All endpoints that require authentication are using HTTPS.

Installation
============

``pip install campbx``

Quick Usage
===========

The API does not require a username and password, however you will have limited access
to only the public endpoints.

Initializing the API::

    from campbx import CampBX
    c = CampBX('username', 'password')

Getting market ticker::

    c.xticker()

    {'Best Ask': '5.17', 'Best Bid': '5.07', 'Last Trade': '5.07'}

Check your account balance::

    c.my_funds()

    {'Liquid BTC': '0.00000000',
     'Liquid USD': '2.19',
     'Margin Account BTC': '0.00000000',
     'Margin Account USD': '0.00',
     'Total BTC': '15.00000000',
     'Total USD': '74.58'}

Check your open orders::

    c.my_orders()

    {'Buy': [{'Dark Pool': 'No',
       'Fill Type': 'Incremental',
       'Margin Percent': 'None',
       'Order Entered': '2012-04-10 08:59:51',
       'Order Expiry': '2012-05-11 00:00:00',
       'Order ID': '239801',
       'Order Type': 'Quick Buy',
       'Price': '4.50',
       'Quantity': '16.00000000',
       'Stop-loss': 'No'}],
     'Sell': [{'Dark Pool': 'No',
       'Fill Type': 'Incr',
       'Margin Percent': 'None',
       'Order Entered': '2012-04-05 22:07:05',
       'Order Expiry': '2012-05-06 00:00:00',
       'Order ID': '215603',
       'Order Type': 'Quick Sell',
       'Price': '5.20',
       'Quantity': '15.00000000',
       'Stop-loss': 'No'}]}

Debug Mode
==========

To turn debug mode on and see more verbose output just use `debug_mode`::

    c.debug_mode(True)

Endpoints
=========

.. toctree::
    :maxdepth: 1
    :glob:

    endpoints/*

Donations
=========

If you would like to donate some coins, please donate to this address, 1EzebDR5wMvnSoQ5KQ1zF6UGcYr8qZSF4v

License
=======

`MIT License <http://www.opensource.org/licenses/mit-license.php>`_

Copyright (c) 2011 Glen Zangirolami

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and 
associated documentation files (the "Software"), to deal in the Software without restriction, including 
without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or 
sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject 
to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial 
portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT 
NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. 
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, 
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE 
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.