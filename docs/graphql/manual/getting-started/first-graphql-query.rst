.. _first_graphql_query:

Making your first GraphQL query
===============================

.. contents:: Table of contents
  :backlinks: none
  :depth: 1
  :local:

Let's create a sample table and query from it using the Hasura console, a UI tool meant for doing exactly this:

Create a table
--------------

Head to the Hasura console, navigate to ``Data -> Create table`` and create a sample table called ``profile`` with
the following columns:

.. code-block:: sql

  profile (
    id INT PRIMARY KEY,
    name TEXT
  )

.. thumbnail:: ../../../img/graphql/manual/getting-started/create-profile-table.png

Now, insert some sample data into the table using the ``Insert Row`` tab of the ``profile`` table.

Try out a query
---------------

Head to the ``GraphiQL`` tab in the console and try running the following query:

.. code-block:: graphql

    query {
      profile {
        id
        name
      }
    }

You'll see that you get all the inserted data!

.. thumbnail:: ../../../img/graphql/manual/getting-started/profile-query.png

Next steps
----------

Read more about:

- :doc:`Building your schema <../schema/index>`
- :doc:`Queries <../queries/index>`

