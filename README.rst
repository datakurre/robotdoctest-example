.. image:: https://secure.travis-ci.org/datakurre/robotdoctest-example.svg?branch=master
   :alt: Travis CI badge
   :target: http://travis-ci.org/datakurre/robotdoctest-example

.. code::

   # Install
   virtualenv env
   source env/bin/activate
   pip install -U pip
   pip install -r requirements.txt

   # Generate docs with screenshots
   ROBOT_BROWSER=phantomjs make html

   # Execute docs as acceptance tests
   pybot -v BROWSER:phantomjs docs
