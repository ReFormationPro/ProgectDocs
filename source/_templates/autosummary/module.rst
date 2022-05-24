{{ fullname | escape | underline }}

Description
-----------

.. automodule:: {{ fullname | escape }}
    :members:

{% if classes %}

Classes
-------
.. autosummary::
    :toctree: _autosummary

    {% for class in classes %}
        {{ class }}
    {% endfor %}

{% endif %}

{% if functions %}
Functions
---------
.. autosummary::
    :toctree: _autosummary

    {% for function in functions %}
        {{ function }}
    {% endfor %}

{% endif %}


Modules
---------
{% if modules %}
.. rubric:: Modules

.. autosummary::
    :toctree: _autosummary
    :recursive:

    {% for item in modules %}
       {{ item }}
    {% endfor %}

{% endif %}