=====
Forum
=====

**Odoo Forum** enables you to connect with your community, give visitors' websites the information
they need and provide outstanding customer satisfaction.

.. important::
   You can manage your forum on both the **frontend** and the **backend**. The **frontend**
   allows you to create a forum quickly from your website, while the **backend** allows you to work
   on it from the :guilabel:`Website` or :guilabel:`eLearning` apps (if enabled), and provides
   access to more advanced configurations.

.. seealso::
   - `Forum product page <https://www.odoo.com/app/forum>`_
   - `eLearning product page <https://www.odoo.com/app/elearning>`_
   - :doc:`Website documentation <website>`

To activate :guilabel:`Forum`, go to :guilabel:`Apps`, search for the :guilabel:`Forum` module, and
install it. A new :guilabel:`Forum` page appears on your website.

.. image:: forum/install-forum.png
   :align: center
   :alt: install Forum

.. _forum/creation:

Forum creation
==============

From your website, click :guilabel:`+NEW`, then on :guilabel:`Forum` to create a new forum. A new
page pops up.

.. image:: forum/new-forum.png
   :align: center
   :alt: create a new forum

Fill in the following information:

- :guilabel:`Forum Name`: add the name of your forum;
- :guilabel:`Forum Mode`: select :guilabel:`Questions` (only one answer allowed) or
  :guilabel:`Discussions` (multiple answers allowed);
- :guilabel:`Privacy`: select :guilabel:`Public` (everyone can access it), :guilabel:`Signed In`
  (your forum is visible for signed in users only), or :guilabel:`Some users` (your forum and its
  content is hidden for non-members of selected group).

Click :guilabel:`SAVE`.

.. tip::
   You can also create a forum from :menuselection:`Website --> Configuration --> Forum: Forums` by
   clicking the :guilabel:`New` button.

New post creation
=================

.. note::
   Only logged-in users can post questions and answer existing ones to avoid one-time participants
   and spam.

To create a new post, click :guilabel:`New Post` and fill in the following information:

- :guilabel:`Title`: add your question or the topic of your post;
- :guilabel:`Description`: add a description for your question. Type "/" to use a command and open
  the :ref:`powerbox <odoo-editor/powerbox>`;
- :guilabel:`Tags`: add :ref:`tags <forum/tags>` to help filter questions and answers related to the
  same topic.

Click :guilabel:`Post Your Question`. A new window pops up inviting you to share your question on
social networks.

Managing posts
==============

Go to the :guilabel:`Forum` page on your website and select the forum you want to access. From
there, you can access the following using the forum's navigation bar:

- :guilabel:`Topics`: :guilabel:`All` topics are displayed by default, but you can refine your
  search by selecting only :guilabel:`Solved`, :guilabel:`Unsolved` or :guilabel:`Unanswered` topics.
- :guilabel:`People`: display users and their :ref:`Karma gains <forum/karma-gains>` (=XP);
  :guilabel:`Badges`, and :guilabel:`Certifications`;
- :guilabel:`Tags`: see the tags used and retrieve questions and discussions based on their tags;
- :guilabel:`Badges`: in addition to building credibility through questions and answers, active
  contributors can be rewarded with :ref:`badges <forum/badges>` according to their participation.
  Badges are visible on both their profile page and their posts;
- :guilabel:`About`: provide guidelines to answer any questions users might have. By default,
  guidelines are available and can be edited according to your need by clicking the :guilabel:`Edit`
  button.

.. _forum/interacting:

Interacting with posts
======================

From a post, users with enough :ref:`Karma gains <forum/karma-gains>` can :guilabel:`answer`,
:guilabel:`comment` and :guilabel:`share` a it on social networks.

They can also :guilabel:`Edit`, :guilabel:`Close`, :guilabel:`Delete`, or :guilabel:`Flag` a post by
clicking ⋮, and :guilabel:`Follow` or :guilabel:`Unfollow` it by clicking the bell.

Moderation tools
================

Use the :guilabel:`Moderation tools` :guilabel:`To validate` posts or to see posts that have been
:guilabel:`Flagged`.

.. image:: forum/moderation-tools.png
   :align: center
   :alt: Select the action button

.. note::
   You need enough karma points to be able to moderate posts. The number of karma points required
   can be updated from the :ref:`Karma Related Rights <forum/karma-related-rights>` tab,
   in the :guilabel:`Moderate posts` field.

Advanced features
=================

.. _forum/forums:

Forums
------

You can manage your forums by going to :menuselection:`Website --> Configuration --> Forum: Forums`.

Click :guilabel:`New` to :ref:`create a forum <forum/creation>` or click an existing one to update
it.

.. tip::
   Get details on your forum's existing posts by clicking the :guilabel:`Posts` smart button. Select
   a post and click the :guilabel:`Action` button to :guilabel:`Export`, :guilabel:`Publish`,
   :guilabel:`Unpublish`, :guilabel:`Archive`, :guilabel:`Unarchive` or :guilabel:`Delete` a
   specific post.

   .. image:: forum/forum-action-button.png
     :align: center
     :alt: Select the action button

Three tabs are available: :ref:`Options <forum/options>`, :ref:`Karma Gains <forum/karma-gains>`,
:ref:`Karma Related Rights <forum/karma-related-rights>`.

.. _forum/options:

Options
~~~~~~~

From this tab you can set the order and visibility of your forum.

- :guilabel:`Default Sort`: Select :guilabel:`Newest`, :guilabel:`Last Updated`,
  :guilabel:`Most Voted`, :guilabel:`Relevance`, or :guilabel:`Answered`.

- :guilabel:`Privacy`:

   - :guilabel:`Public`: your forum is public;
   - :guilabel:`Signed in`: your forum is visible for signed in users;
   - :guilabel:`Some users`: your forum and its content are hidden from non-members of the
     authorized group.

You also have the possibility to add a short :guilabel:`Description visible on your website`.

.. _forum/karma-gains:

Karma gains
~~~~~~~~~~~

Karma points are given to the forum's active participants to keep them involved and provide them
access to functionalities like voting, commenting, and editing when they reach a certain Karma
level.

The number of points is set by default. You can modify it by clicking it.

.. note::
   Each new user automatically receives three points when their e-mail address is validated.

.. tip::
   If you have the **eLearning** app, completing quizzes can grant you points.

.. _forum/karma-related-rights:

Karma-related rights
~~~~~~~~~~~~~~~~~~~~

Karma rights are used to determine what a user can and cannot do, like access rights.

Go to the :guilabel:`Karma Related Rights` tab to set up a moderation system with Karma points to
give your most active members access to more functionalities and to reduce spamming messages. Click
a number to edit it.

.. _forum/ranks:

Ranks
-----

Ranks are used to differentiate users based on their Karma level.

You can manage :guilabel:`Ranks` by going to :menuselection:`Website --> Configuration --> Forum:
Ranks`. Click :guilabel:`New` to create a new rank. Fill in the :guilabel:`Rank Name`, add the
:guilabel:`Required Karma`, a :guilabel:`Description` and if you want, fill in the
:guilabel:`Motivational` tab to encourage users that reach this rank.

.. _forum/tags:

Tags
----

:guilabel:`Tags` can be managed by going to :menuselection:`Website --> Configuration --> Forum:
Tags`. Click :guilabel:`New` to create a new tag, and select the :guilabel:`Forum` it is related to.

.. _forum/badges:

Badges
------

Grant badges to your members for their questions, answers, shares, likes, and votes to reward the
most active ones. Badges appear on their profile page and on their posts. Badges can be managed by
going to :menuselection:`Website --> Configuration --> Forum: Badges`.

.. _forum/close-reasons:

Close reasons
-------------

You can retrieve your posts' close reasons by going to :menuselection:`Website --> Configuration
--> Forum: Close Reasons`.

.. note::
   :ref:`Close <forum/interacting>` a post directly from the question or discussion, by clicking the
   ⋮, and :guilabel:`Close`.
