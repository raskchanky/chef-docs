.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``GET`` method is used to get a specific version of a cookbook. Use ``latest`` to get the most recent version of a cookbook.

This method has no parameters.

**Request**

.. code-block:: xml

   GET /cookbooks/COOKBOOK_NAME/versions/latest

Or:

.. code-block:: xml

   GET /cookbooks/COOKBOOK_NAME/versions/VERSION

**Response**

The response will return details for a cookbook version, including the license under which the cookbook is distributed, the most recent update, version, URI, date of cookbook creation, path to the cookbook's |tar gz| file, its dependencies and platforms it supports and so on:

.. code-block:: ruby

  {
    "license": "Apache 2.0",
    "tarball_file_size": 18553,
    "version": "2.4.0",
    "average_rating": null,
    "cookbook": "http://supermarket.getchef.com/api/v1/cookbooks/apt",
    "file": "http://supermarket.getchef.com/api/v1/cookbooks/apt/versions/2_4_0/download",
    "dependencies": {},
    "platforms": {
      "debian": ">= 0.0.0",
      "ubuntu": ">= 0.0.0"
    }
  }

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - |response code 200 ok| The requested cookbook exists.
   * - ``400``
     - |response code 400 unsuccessful| The requested cookbook does not exist. For example:
       ::

          {
             "error_messages":
             ["Resource does not exist"],
             "error_code": "NOT_FOUND"
          }
