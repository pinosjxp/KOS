.. _element:

Element
======

An element is a docked component of a :struct:`Vessel` 

.. note::
        Element boundries are not formed between two docking ports that were launched coupled. a craft with such an arrangement will appear as one element until you uncoupled the nodes and redocked

.. structure:: Element

    ===================================== ========================= =============
     Suffix                                Type                      Description
    ===================================== ========================= =============
     :attr:`NAME`                          string                    The name of the docked craft
     :attr:`UID`                           string                    Unique Identifier 
     :attr:`PARTS`                         :struct:`List`            all :struct:`Parts <Part>`
     :attr:`RESOURCES`                     :struct:`List`            all :struct:`AggrgateResources <AggregateResource>`
    ===================================== ========================= =============

.. attribute:: Element:UID

    :type: string
    :access: Get only 

    A unique id

.. attribute:: Element:NAME

    :type: string
    :access: Get/Set

    The name of the Element element, is an artifact from the vessel the element belonged to before docking. Cannot be set to an empty string.

.. attribute:: Element:PARTS

    :type: :struct:`List` of :struct:`Part` objects
    :access: Get only

    A List of all the :ref:`parts <part>` on the Element. ``SET FOO TO SHIP:PARTS.`` has exactly the same effect as ``LIST PARTS IN FOO.``. For more information, see :ref:`ship parts and modules <parts and partmodules>`.

.. attribute:: Element:RESOURCES

    :type: :struct:`List` of :struct:`AggregateResource` objects
    :access: Get only

    A List of all the :ref:`AggregateResources <AggregateResource>` on the element.
