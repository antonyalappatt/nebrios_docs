Schedule
========

These are related to Drips but serve a different purpose. Schedules allow you to wake a script up on a repeating schedule and try to run against **every** PID in the system. This is useful for monitoring processes within your system, making sure they are moving along, aren't missing anything, and for many other uses. :doc:`../admin/drips` on the other hand add data to your system on a schedule you define.

Simply use cron syntax inside of the schedule variable:

:: 

   schedule = "0 0 * * *" # daily 

It replaces **listens_to** and belongs in the top of your script; the :doc:`../scripts/registration` area.


Here's a quick reminder of Cron syntax:

::

    * * * * * command to be executed
    - - - - -
    | | | | |
    | | | | ----- Day of week (0 - 7) (Sunday=0 or 7)
    | | | ------- Month (1 - 12)
    | | --------- Day of month (1 - 31)
    | ----------- Hour (0 - 23)
    ------------- Minute (0 - 59)

.. note:: the @monthly/@daily keyword syntax isn't recognized right now




