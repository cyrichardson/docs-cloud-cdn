.. _cdn-delete-a-service:

Delete a service
~~~~~~~~~~~~~~~~

.. code::

    DELETE /v1.0/{project_id}/services/{service_id}

This operation deletes the specified service.

The following table shows the possible response codes for this operation.

+--------------------------+-------------------------+------------------------+
|Response Code             |Name                     |Description             |
+==========================+=========================+========================+
|202                       |Accepted                 |The request has been    |
|                          |                         |fulfilled, but does not |
|                          |                         |return a representation |
|                          |                         |(that is, the response  |
|                          |                         |is empty).              |
+--------------------------+-------------------------+------------------------+

Request
-------

The following table shows the URI parameters for the request.

+-------------+-------------+-------------------------------------------------+
|Name         |Type         |Description                                      |
+=============+=============+=================================================+
|{project_id} |String       |The project ID for the user. If you do not set   |
|             |             |the ``X-Project-Id header`` in the request, use  |
|             |             |``project_id`` in the URI. For example: ``GET    |
|             |             |https://global.cdn.api.rackspacecloud.com/v1.0/  |
|             |             |{project_id}``                                   |
+-------------+-------------+-------------------------------------------------+
|{service_id} |String       |Specifies the service ID that represents         |
|             |             |distributed content. The value is a UUID, such as|
|             |             |96737ae3-cfc1-4c72-be88-5d0e7cc9a3f0, that is    |
|             |             |generated by the server.                         |
+-------------+-------------+-------------------------------------------------+

This operation does not accept a request body.

**Example: Delete a service HTTP request**

.. code::

   DELETE /v1.0/110011/services/96737ae3-cfc1-4c72-be88-5d0e7cc9a3f0 HTTP/1.1
   Host: global.cdn.api.rackspacecloud.com
   X-Auth-Token: 0f6e9f63600142f0a970911583522217
   Content-Type: application/json

Response
--------

This operation does not return a response body.

**Example: Delete a service HTTP response**

.. code::

   HTTP/1.1 202 Accepted
