---
title: 'HOWTO: Refresh the Task Widget on the Summary Tab'
description: 'Learn how to update the workflow widget data on the Summary tab'
review:
    comment: ''
    date: '2019-11-05'
    status: ok
details:
    howto:
        excerpt: Learn how to refresh the task widget on the Summary tab.
        level: Advanced
        tool: Studio
        topics: 'Workflows, Widget'
labels:
    - lts2016-ok
    - widget
    - atchertchian
    - howto
    - workflow
    - excerpt
    - content-review-lts2017
confluence:
    ajs-parent-page-id: '19235619'
    ajs-parent-page-title: Workflow How-To Index
    ajs-space-key: NXDOC
    ajs-space-name: Nuxeo Platform Developer Documentation
    canonical: How+to+Refresh+the+Task+Widget+on+the+Summary+Tab
    canonical_source: 'https://doc.nuxeo.com/display/NXDOC/How+to+Refresh+the+Task+Widget+on+the+Summary+Tab'
    page_id: '12915679'
    shortlink: 3xPF
    shortlink_source: 'https://doc.nuxeo.com/x/3xPF'
    source_link: /display/NXDOC/How+to+Refresh+the+Task+Widget+on+the+Summary+Tab
tree_item_index: 500
history:
    -
        author: Solen Guitter
        date: '2015-04-24 09:11'
        message: 'eplace operation User Interface >Refresh with User Interface > Raise Seam event'
        version: '7'
    -
        author: Solen Guitter
        date: '2014-12-01 21:49'
        message: ''
        version: '6'
    -
        author: Manon Lumeau
        date: '2014-09-09 18:08'
        message: ''
        version: '5'
    -
        author: Manon Lumeau
        date: '2014-09-09 18:01'
        message: ''
        version: '4'
    -
        author: Solen Guitter
        date: '2013-07-17 22:32'
        message: ''
        version: '3'
    -
        author: Alain Escaffre
        date: '2013-04-22 11:45'
        message: ''
        version: '2'
    -
        author: Alain Escaffre
        date: '2013-04-22 11:42'
        message: ''
        version: '1'

---

If you start a workflow automatically using the [Workflow > StartWorkflow](http://explorer.nuxeo.org/nuxeo/site/distribution/latest/viewOperation/Context.StartWorkflow) operation and that your workflow's first node creates a task to the workflow initiator, you need to use in the input chain the **[User Interface > Raise Seam events](http://explorer.nuxeo.com/nuxeo/site/distribution/latest/viewOperation/Seam.RaiseEvents)** operation, with the value `workflowNewProcessStarted` for the event name.

If you cancel a workflow automatically using the [Workflow > CancelWorkflow](http://explorer.nuxeo.com/nuxeo/site/distribution/server-10.10/viewOperation/WorkflowInstance.Cancel) operation, you need to use in the input chain the **[User Interface > Raise Seam events](http://explorer.nuxeo.com/nuxeo/site/distribution/latest/viewOperation/Seam.RaiseEvents)** operation, with the value `WorkflowInstance.Cancel` for the event name.

* * *

<div class="row" data-equalizer data-equalize-on="medium"><div class="column medium-6">{{#> panel heading='Related How-Tos'}}

- [HOWTO: Modify a Workflow Variable outside of Workflow Context]({{page page='how-to-modify-a-workflow-variable-outside-of-workflow-context'}})
- [HOWTO: Make a Simple Task Assignment to One or Many Users]({{page page='how-to-make-a-simple-task-assignment-to-one-or-many-users'}})
- [How-To Index]({{page page='how-to-index'}})

{{/panel}}</div><div class="column medium-6">{{#> panel heading='Related Documentation'}}

- [Workflow in Nuxeo Studio]({{page space='studio' page='workflow'}})
- [Full-Text Queries]({{page page='full-text-queries'}})
- [NXQL]({{page page='nxql'}})
- [Variables Available in the Automation Context]({{page page='variables-available-in-the-automation-context'}})
- [Workflow]({{page page='workflow'}})

{{/panel}}</div></div>
