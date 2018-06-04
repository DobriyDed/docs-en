About
=======

How does CSMM work?
--------------------

At the very basic level, CSMM communicates with your server via the web API provided by Allocs fixes. CSMM uses telnet once during set up to create authentication details. Telnet info is never stored in the database!

Once that has happened, CSMM uses a `custom library <https://github.com/niekcandaele/machinepack-7Days-webapi/>`_ to get/set/format/... data. 