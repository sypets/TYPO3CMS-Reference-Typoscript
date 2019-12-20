.. include:: ../Includes.txt


.. _setup:
.. _top-level-objects:

=================
Top-level objects
=================

.. container:: ts-properties

   ======================== ================== ====================== =======
   Top-level object         Data Type          :ref:`stdwrap`         Default
   ======================== ================== ====================== =======
   ``page, ...``            :ref:`page`
   `config`_                :ref:`config`
   `constants`_             :ref:`constants`
   `Other reserved TLO's:`_ *(whatever)*
   `resources`_             readonly
   `sitetitle`_             readonly
   `types`_                 readonly
   ======================== ================== ====================== =======

.. ### BEGIN~OF~TABLE ###



.. container:: table-row

   Property
         page, ...

   Data type
         :ref:`page`

   Description
         Start a new page.

         **Example:** ::

            page = PAGE
            page.typeNum = 1

         **Guidelines:**

         Good, general :ts:`PAGE` object names to use are such as:

         *page* for the main page with content

         *json* for a json stream with content

         *xml* for a XML stream with content

         These are just recommendations. However, especially the name :ts:`page`
         for the content bearing page is very common and most documentation will
         imply that your main page object is called :ts:`page`.


.. _top-level-objects-config:

config
======

.. container:: table-row

   Property
         config

   Data type
         :ref:`config`

   Description
         Global configuration.

         These values are stored with cached pages which means they are also
         accessible when retrieving a cached page.




.. _top-level-objects-constants:

constants
=========

.. container:: table-row

   Property
         constants

   Data type
         :ref:`constants`

   Description
         Site-specific constants, e.g. a general email address. These constants
         may be substituted in the text throughout the pages. The substitution
         is done by :ref:`parsefunc` (with :ts:`constants = 1` set).



.. _top-level-objects-other-reserved-tlo-s:

Other reserved TLO's:
=====================

.. container:: table-row

   Property
         Other reserved TLO's:

         plugin

         tt\_\*

         temp

         styles

         lib

         \_GIFBUILDER

   Data type
         *(whatever)*

   Description
         These top-level object names are reserved. That means you can risk
         static\_templates to use them:

         :ts:`plugin` is used for rendering of special content like boards,
         e-commerce solutions, guestbooks and so on. Normally set from
         static\_templates.

         :ts:`tt_`, e.g. :ts:`tt_content` (from "content (default)") is used to
         render content from tables.

         :ts:`temp` and :ts:`styles` are used for code-libraries you can
         copy during parse-time, but they are not saved with the template in
         cache. :ts:`temp` and :ts:`styles` are unset before the template is
         cached! Therefore use these names to store temporary data.

         :ts:`lib` can be used for a "library" of code, you can reference in
         TypoScript (unlike :ts:`styles` which is unset).



.. _top-level-objects-resources:

resources
=========

.. container:: table-row

   Property
         resources

   Data type
         readonly

   Description
         Resources in list (internal)



.. _top-level-objects-sitetitle:

sitetitle
=========

.. container:: table-row

   Property
         sitetitle

   Data type
         readonly

   Description
         SiteTitle (internal)



.. _top-level-objects-types:

types
=====

.. container:: table-row

   Property
         types

   Data type
         readonly

   Description
         Types (internal)

         :ts:`type=99` reserved for plaintext display


.. ###### END~OF~TABLE ######

.. toctree::
   :hidden:

   ../Page/Index


.. toctree::
   :maxdepth: 5
   :titlesonly:
   :glob:

   ../Setup/Top-levelObjects/Index
   ../Setup/Plugin/Index
   ../Setup/Config/Index
   ../Setup/Constants/Index
   ../Setup/Page/Index
