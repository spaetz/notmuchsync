.. notmuch documentation master file, created by
   sphinx-quickstart on Tue Feb  2 10:00:47 2010.

.. currentmodule:: notmuchweb.notmuch

Welcome to notmuch's documentation!
===================================

The :mod:`notmuch` module provides an interface to the `notmuch <http://notmuchmail.org>`_ functionality. The main work horse of this module is the class :class:`Notmuch` with important other classes representing a :class:`Thread` and a single :class:`Message`.

   .. note:: The current code assumes that  you have the dateparser branch applied. It also assumes that the patch is included to send the notmuch tags as json arrays. If the latter has not, I have been experiencing weird json parsing failures.

   .. TODO: Provide fallbacks if the dateparser branch has not been applied.

   .. TODO: Provide fallbacks if notmuch tags are not sent with the json.

.. moduleauthor:: Sebastian Spaeth <Sebastian@SSpaeth.de>

:License: This module is covered under the GNU GPL v2 (or later).

This page contains the main API overview. More information on specific topics can be found on the following pages:

.. toctree::
   :maxdepth: 1



:mod:`notmuch` -- The Notmuch interface
=============================================
.. currentmodule:: notmuchweb.notmuch

:class:`Message` -- A single email message
------------------------------------

.. autoclass:: Message
   :members:

:class:`Thread` -- Represents a message thread
-----------------------------------------------

.. autoclass:: Thread
   :members:

   .. note:: A Thread is what a call to notmuch.show() will return, containing a bunch of :class:`Message`\ s.

:class:`Notmuch` -- A notmuch call
------------------------------------

.. autoclass:: Notmuch
   :members:

   .. data: '__notmuchcmd__'

      This is the actual binary that will be executed in order to run a notmuch command. This is set to *notmuch* and should usually not be changed.

:exc:`NotmuchError` -- A Notmuch execution error
------------------------------------------------
.. autoexception:: NotmuchError
   :members:

   This execption inherits directly from :exc:`Exception` and is raised on errors during the notmuch execution.

Indices and tables
==================

* :ref:`genindex`
* :ref:`search`

