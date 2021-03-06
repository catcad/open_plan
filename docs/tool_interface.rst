.. _tool_interface:

**************************
Tool interface description
**************************

Concepts definition
===================

In order to describe the interface, a few definitions are required at first.

.. _view-def:

view
----
    Description of a given state of the user interface: what should the user be able to interact with in that *view*, which other *view* can the user visit from the current *view*. The collection of *views* form together the user interface. Note: the view does not describe how the interface looks like to the user, this is described in the *view-rendering*.

.. _view-component-def:

view-component
--------------
    A *view-component* is a part of a *view* which can be described independently from the view and could be reused in different *views* (a menu bar for example). A *view-component* is described in terms of its attributes and its actions. For example a menu bar has a nested list of items (each item can itself be a list of item: submenus). Each item, if not itself a list, consists of a label (what the user will see) and an action (what will be done upon clicking/selecting the item).

.. _attribute-def:

attribute
---------
    An attribute contains the essential information needed to characterize and render a :ref:`view-def` or a :ref:`view-component-def`. An attribute might be visible in the :ref:`view-def` or :ref:`view-component-def` but it can also just be information. An attribute can be linked to a certain number of :ref:`action-def` and to certain :ref:`requirement-def`.

.. _action-def:

action
------
    An action describes what the user can do in a certain :ref:`view-def` or :ref:`view-component-def`. Each action has an index which is used to link it to an :ref:`attribute-def`.
Example: [index] The user can click on button B to trigger action C

.. _requirement-def:

requirement
------------
A requirement describes specific conditions of a :ref:`view-def`, a :ref:`view-component-def`, an :ref:`action-def` or an :ref:`attribute-def` that should be met. Each requirement has an index which is used to link it to an :ref:`attribute-def`.
 Example: [index] The button B cannot be clicked unless text input C is not filled by user.

.. _view-rendering-def:

view-rendering
--------------
    Description of how a *view* or *component-view* will be rendered on the screen. This belongs to frontend and is where the details about color, size, font, placement on screen matter. For example a menu bar which is a *view-component* can have many different *view-rendering* (horizontal with buttons, expandable vertically only on hover, etc.).

.. _energy-type-def:

energy type
-----------
    An energy type is represented by a bus. It describes the energy carrier for an energy sector: heat, electricity, gas, biomass, H2O.

.. _main-window-def:

main window
-----------
    It is the window from which the user can interact with the open_plan tool on their computer.


.. _widget-def:

widget
------
    Smaller window within the tool's :ref:`main-window-def`.
    A *widget* can be moved around by the user within the :ref:`main-window-def` and collapsed into another *widget* (then each *widget* is accessible via tabs).

.. _views-label:

Views definition
================

.. contents::
   :local:
   :depth: 1

----

.. _landing-label:

.. include:: views/landing.rst


----

.. _scenario_comparison-label:

.. include:: views/scenario_comparison.rst


View-components definition
==========================

.. contents::
   :local:
   :depth: 1

.. it is important to have a blank line before and after the ----, otherwise the reference does not work!


----

.. _welcome-label:

.. include:: view_components/welcome.rst

----

.. _progression_bar-label:

.. include:: view_components/progression_bar.rst

----

.. _menu_bar-label:

.. include:: view_components/menu_bar.rst

----

.. _create_project-label:

.. include:: view_components/create_project.rst

----

.. _load_project-label:

.. include:: view_components/load_project.rst

----

.. _create_scenario-label:

.. include:: view_components/create_scenario.rst

----

.. _load_scenario-label:

.. include:: view_components/load_scenario.rst

----

.. _input_parameter_field-label:

.. include:: view_components/input_parameter_field.rst

----

.. _load_input_dataseries-label:

.. include:: view_components/load_input_dataseries.rst

----

.. _scenario_parameters-label:

.. include:: view_components/scenario_parameters.rst

----

.. _project_parameters-label:

.. include:: view_components/project_parameters.rst

----

.. _es_sector_selector-label:

.. include:: view_components/energy_system_sector_selector.rst

----

.. _es_network-label:

.. include:: view_components/energy_system_network.rst

----

.. _es_component-label:

.. include:: view_components/energy_system_component.rst

----

.. _export_project-label:

.. include:: view_components/export_project.rst

----

.. _view_specific_documentation-label:

.. include:: view_components/view_specific_documentation.rst

----

.. _visualize_dataseries-label:

.. include:: view_components/visualize_dataseries.rst


Abstract-components Definition
==============================


.. contents::
   :local:
   :depth: 1

----

.. _scenario-label:

.. include:: abstract_components/scenario.rst
