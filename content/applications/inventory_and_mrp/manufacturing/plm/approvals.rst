=========
Approvals
=========

.. |ECO| replace:: :abbr:`ECO (Engineering Change Order)`
.. |ECOs| replace:: :abbr:`ECOs (Engineering Change Orders)`

.. _plm/approvals:

Notify stakeholders and managers automatically by assigning approvers to stages in :ref:`engineering
change orders <plm/eco>` (ECOs) for review. Changes can only be applied after the assigned approver
accepts them. Approvals ensure reviews by team members, preventing mistakes and premature actions.

.. seealso::
    :ref:`Stage configuration <plm/eco/stage-config>`

Add approver
============

To add an approver, first go to the :menuselection:`PLM app` and click on the ECO type project card
to open the Gantt view of the |ECOs|. On the :guilabel:`Engineering Change Orders` page, hover over
the intended stage, and select the :guilabel:`⚙️ (gear)` icon. Then, click :guilabel:`Edit` to open
a pop-up window.

.. note::
   Approvers can be added to any stage, but it's strongly recommended to assign them to the
   *verification* stage, which comes before the *closing* stage where |ECOs| are applied and the
   :abbr:`BoM (Bill of Materials)` version is updated. Read more about :ref:`stage types, here
   <plm/eco/stage-config>`.

.. _plm/approvals/approval-type:

In the :guilabel:`Edit` stage pop-up, click the :guilabel:`Add a line` button under
:guilabel:`Approvals`. Type in the approver's position or title under :guilabel:`Role` (e.g.
"Engineering Manager", "Quality Team"), and select the relevant :guilabel:`User` from the drop-down
menu. Set the :guilabel:`Approval Type` to :guilabel:`Is required to approve`, :guilabel:`Approves,
but the approval is optional`, or :guilabel:`Comments only`.

.. example::
   Assign the `CTO`, "Mitchell Admin" as a required approver for |ECOs| in the `Validated` stage in
   the `New Product Introduction` ECO type. Approvals from the quality and marketing teams are not
   required to apply changes to the |ECO| because their :guilabel:`Approval Type` is set to
   :guilabel:`Approves, but the approval is optional` and :guilabel:`Comments only`, respectively.

   .. image:: approvals/approvers.png
      :align: center
      :alt: Set an approver that "Is required to approve" ECOs in the "Validated" stage.

Manage approvals
================

Approvers can easily track their to-do approvals by navigating to the :menuselection:`PLM app` and
looking at the ECO type card, which shows the count of open tasks assigned to them. Here's what each
button on the ECO type card does:

#. :guilabel:`X Engineering Changes` button displays a count of in-progress |ECOs| of this ECO type.
   Clicking the button opens the Gantt view of the :guilabel:`Engineering Change Orders` page.

#. :guilabel:`My Validations` displays a count of |ECOs| that the approver must accept or reject.
   Clicking on this button displays |ECOs| pending approval or rejected (marked with the red
   :guilabel:`Blocked` blocked state).

#. :guilabel:`All Validations` displays a count of |ECOs| a verification stage pending approval from
   any approvers. Clicking on the button displays |ECOs| pending approval from or rejected by any
   approver.

#. :guilabel:`To Apply` displays a count of |ECOs| the user needs to apply changes to. Clicking on
   the button displays all the |ECOs| to approve and apply changes to in the verification stage.
   |ECOs| marked with the green :guilabel:`Done` stage have already been approved, and the user just
   needs to click on the |ECO| to enter the form view and click the :guilabel:`Apply Changes`
   button.

.. image:: approvals/validation-overview.png
   :align: center
   :alt: Display count of validations to-do and buttons to open filtered list of ECOs.

Approve ECOs
------------

Navigate to an |ECO| in a verification stage while logged in as the assigned approval to see the
:guilabel:`Approve`, :guilabel:`Reject`, and :guilabel:`Apply Changes` button. To approve the |ECO|
and apply the changes onto the production :abbr:`BoM (Bill of Materials)`, click :guilabel:`Approve`
then :guilabel:`Apply Changes`. Note that the :guilabel:`Apply Changes` button will not work unless
the :guilabel:`Approve` button was pressed first. Additionally, the chatter will log the history of
the buttons pressed.

.. warning::
   When the :guilabel:`Approval Type` is **not** set to :guilabel:`Is required to approve`, approval
   from the associated user is not needed before applying changes with the the :guilabel:`Apply
   Changes` button. Thus, the :guilabel:`Apply Changes` **will work** without the requiring the
   :guilabel:`Approve` button to be pressed first. pressed before it.


Automated activities
--------------------

When an |ECO| is moved to a verification stage, a planned activity is automatically created for
assigned approvers to review the |ECO|. Approvers receive a notification in their activities inbox,
accessible through the :guilabel:`🕘 (clock)` icon at the top of the page. In to-do task list, the
:guilabel:`Engineering Change Order (ECO)` notification displays the amount of :guilabel:`Late`,
:guilabel:`Today`'s, and :guilabel:`Future` activities. Clicking on each of these buttons shows a
filtered Gantt view of the respective |ECOs|.

.. example::
   Scheduled activities are shown in the :guilabel:`🕘 (clock)` icon, with `5` |ECOs| pending
   approval :guilabel:`Today`. Currently, there are `0` :guilabel:`Late` or :guilabel:`Future`
   |ECOs|.

    .. image:: approvals/todo-list.png
       :align: center
       :alt: Show scheduled approvals notifications for the user.

Click each pending |ECO|, and a *planned activity* for :guilabel:`ECO Approval` is recorded in the
chatter. Clicking on the :guilabel:`i (Info)` icon to view additional information, including the
approval's :guilabel:`Created` date, the approver :guilabel:`Assigned to` it, and the due date.

.. image:: approvals/planned-activity.png
   :align: center
   :alt: Show additional details of the planned ECO approval.

Follow-up activities
~~~~~~~~~~~~~~~~~~~~

When |ECOs| are rejected, tasks need be assigned project members for required modifications before
|ECO| approval. To create tasks with deadlines, navigate to the rejected |ECO| form and go to the
chatter. Select the :guilabel:`Mark Done` button in the :guilabel:`Planned Activities` section of
the chatter to close the activity and open a pop-up window for creating tasks.

.. image:: approvals/mark-as-done.png
   :align: center
   :alt: Show *Mark Done* window to show *Done & Schedule Next*, *Done*, and *Discard* buttons to
         close the planned activity.

In the :guilabel:`Mark Done` window, click :guilabel:`Done & Schedule Next` to open a new
:guilabel:`Schedule an Activity` window. Next, set the :guilabel:`Assigned to` team member and the
:guilabel:`Due Date` for completing the changes. Provide task details in the :guilabel:`Summary`
field and the text box. Click the :guilabel:`Schedule` button to close the window.

After closing the window, on the |ECO| form, move the |ECO| back one stage. Doing so ensures that
when the team member completes the changes and returns the |ECO| to the verification stage, a new
:guilabel:`ECO Approval` task is created for the approver.

.. example::

   The approver creates an activity for the :guilabel:`Responsible` of the |ECO|, `Laurie Poiret`,
   that details the changes required for the approver to :guilabel:`Accept` the |ECO|. Clicking the
   :guilabel:`Schedule` button creates a planned activity for Laurie due on `08/15/2023`.

   .. image:: approvals/schedule-an-activity.png
      :align: center
      :alt: Create a scheduled activity for follow-up changes to a rejected ECO.
