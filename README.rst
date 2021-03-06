Lumberjack - Python Logging for Humans™
#######################################

What is this?
=============

This project is about creating a custom logger with a few arguments such as logger name and file path (if FileHandler is used).


Why was this made?
==================

In the python projects I have worked with (work or personal projects), I have always had to create a logging instance with a FileHandler, provide a logging format, provide logging file name (and create directories if need be), which is extremely frustrating, at the least. So I decided to encapsulate the pain points regarding the aforementioned.



How do I use this?
==================

- Importing package

.. code-block:: python

    from lumberjack import Lumberjack

    # outputs logs in the console.
    logger = Lumberjack(name="lumberjack")

    # outputs logs in the filename 'logs/lumberjack_<timestamp>.log'
    logger = Lumberjack(name="lumberjack", file_name="logs/lumberjack.log")


- Calling ``.info(...)``

.. code-block:: python

    logger.info('Live long and prosper, hoomans')

    # Log info output
    2017-02-23 20:31:41,932 - lumberjack - INFO - Live long and prosper, hoomans!

- Calling ``.debug(...)``
.. code-block:: python

    logger.debug('NOOOOOOOOOOOOOOOOO!')

    # Log debug output
    2017-02-24 04:08:11,265 - lumberjack - DEBUG - NOOOOOOOOOOOOOOOOO!

- Calling ``.log(...)``
.. code-block:: python

    logger.log(50, 'This is DEFCON level 50')

    # Log output
    2017-02-24 04:33:22,869 - lumberjack - CRITICAL - This is DEFCON level 50

    logger.log(500, 'Deez notes were demonetized in India')

    # Log output
    2017-02-24 04:33:48,558 - lumberjack - Level 500 - Deez notes were demonetized in India

    logger.log('This is DEFCON level 999?')

    # Log output
    2017-02-24 04:33:13,615 - lumberjack - Level 999 - This is DEFCON level 999?


Can I contribute to this?
=========================

Sure! Create an issue in the repo if it's not already present. Then fork this repo, branch off from `master`, add a feature / push a fix and raise a pull-request. I'll merge it once I deem it useful.
