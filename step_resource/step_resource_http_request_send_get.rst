.. This is an included how-to. 

.. To send a GET request:

.. code-block:: ruby

   http_request "some_message" do
     url "http://example.com/check_in"
   end

The message is sent as "http://example.com/check_in?message=some_message".
