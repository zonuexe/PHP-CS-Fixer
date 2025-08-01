========================
Rule ``empty_loop_body``
========================

Empty loop-body must be in configured style.

Configuration
-------------

``style``
~~~~~~~~~

Style of empty loop-bodies.

Allowed values: ``'braces'`` and ``'semicolon'``

Default value: ``'semicolon'``

Examples
--------

Example #1
~~~~~~~~~~

*Default* configuration.

.. code-block:: diff

   --- Original
   +++ New
   -<?php while(foo()){}
   +<?php while(foo());

Example #2
~~~~~~~~~~

With configuration: ``['style' => 'braces']``.

.. code-block:: diff

   --- Original
   +++ New
   -<?php while(foo());
   +<?php while(foo()){}

Rule sets
---------

The rule is part of the following rule sets:

- `@PhpCsFixer <./../../ruleSets/PhpCsFixer.rst>`_
- `@Symfony <./../../ruleSets/Symfony.rst>`_ with config:

  ``['style' => 'braces']``

References
----------

- Fixer class: `PhpCsFixer\\Fixer\\ControlStructure\\EmptyLoopBodyFixer <./../../../src/Fixer/ControlStructure/EmptyLoopBodyFixer.php>`_
- Test class: `PhpCsFixer\\Tests\\Fixer\\ControlStructure\\EmptyLoopBodyFixerTest <./../../../tests/Fixer/ControlStructure/EmptyLoopBodyFixerTest.php>`_

The test class defines officially supported behaviour. Each test case is a part of our backward compatibility promise.
