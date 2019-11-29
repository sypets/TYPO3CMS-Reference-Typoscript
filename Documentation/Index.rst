.. include:: Includes.txt


.. _start:

=============================
TypoScript Template Reference
=============================


.. Note for editors: This is a summary of the Introduction
..   It should give the reader a notion of what this manual
..   is about and include most important points and links,
..   but should not dive into the details

The **TypoScript Template Reference (TSref)** is a reference for the core content objects,
properties and functions available for template building in TYPO3 using the
TypoScript template engine.

Read the :ref:`introduction` for more information about TypoScript Templates.

Quick Links
===========

:ref:`config` | :ref:`cobj-fluidtemplate` | :ref:`page`

Other manuals: :ref:`TypoScript Syntax ➜ <t3coreapi:typoscript-syntax-start>`

What are TypoScript Templates?
==============================

.. ideally add a picture and explanation how the components of TYPO3
..   work together: TSFE, Fluid, FLUIDTEMPLATE

* TSFE
* What about Fluid?
* FLUIDTEMPLATE

What Can You do With TypoScript Templates
=========================================

*

TypoScript vs. Fluid
====================

* If Fluid is TYPO3 templating engine, what is TypoScript for?
* Will TypoScript disappear in the future?


TypoScript vs. TSconfig
=======================

TypoScript - as used in **TypoScript templates** - and **TSconfig** are not
the same thing. While both use the *TypoScript syntax language*,
:ref:`TSconfig <t3tsconfig:start>` is used to customize the TYPO3 backend
while TypoScript Templates are used in the frontend as templating and
configuration language.

You cannot use the Content objects and properties described here to configure
TSconfig.

TypoScript Templates vs. TypoScript Syntax
==========================================

For explanations about the TypoScript syntax itself, please refer
to the :ref:`TypoScript Syntax in "TYPO3 Explained" <t3coreapi:typoscript-syntax-start>`.

Constants & Setup
=================

TypoScript templates consist of a clearly separated constants and setup section.

For constants:

* *TypoScript constant syntax* is used
* Values are assigned to variables that may be used in the TypoScript setup

For setup:

* :ref:`TypoScript syntax language <t3coreapi:typoscript-syntax-start>` is used


.. ... end of introduction summary ...



TYPO3 Version
=============

This version of the manual always refers to the latest released TYPO3 version. For
older versions, use the version selector at the bottom left of the site.

For new features, this reference includes a note in which TYPO3 version the
feature was added. If such a note is missing, the feature is part of TYPO3 since
version 7.6 at least.

.. _case-sensitivity:

Case sensitivity
================

All names and references in TypoScript are **case sensitive!** This
is very important to notice. For example watch the words "TEXT" and "value"
in this TypoScript code::

   myObject = TEXT
   myObject.value = <strong>Some HTML code</strong>

This is not the same as ::

   myObject = text
   myObject.Value = <strong>Some HTML code</strong>

While the first will be recognized as the content object "TEXT" and
will produce the desired output, the latter will not be recognized and
will not output anything. Even if you wrote **"TEXT"** in uppercase in the
second example, it would still not work, because the property **"value"**
is misspelled.

Always remember: In this manual the case of objects **is** important.


.. toctree::
   :hidden:

   Introduction/Index
   UsingSetting/Index
   DataTypes/Index
   ObjectsAndProperties/Index
   Conditions/Index
   Functions/Index

.. toctree::
   :caption: TypoScript Objects
   :hidden:

   Setup/Index
   ContentObjects/Index
   Gifbuilder/Index
   MenuObjects/Index

.. toctree::
   :caption: Appendix
   :hidden:

   AppendixA/Index
   Sitemap/Index
   About
   Targets
