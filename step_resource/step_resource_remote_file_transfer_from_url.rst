.. This is an included how-to. 

.. To transfer a file from a URL:

.. code-block:: ruby

   remote_file "/tmp/testfile" do
     source "http://www.example.com/tempfiles/testfile"
     mode "0644"
     checksum "3a7dac00b1" # A SHA256 (or portion thereof) of the file.
   end
