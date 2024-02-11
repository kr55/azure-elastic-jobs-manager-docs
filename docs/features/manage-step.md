---
layout: default
title: Manage step
parent: Manage job
grand_parent: Documentation
permalink: /docs/features/manage-job/manage-step/
---
# Job Properties - Creating Steps

## Overview
This document provides instructions on how to create steps within job properties using the 'testjob' interface.

## Interface Elements
- **Select a page**: Navigation pane including 'General', 'Steps', and 'Schedule'.
- **Script & Help**: Buttons for additional options and assistance.
- **Job step list**: A table displaying the steps, including columns for Step, StepName, Credential, TargetGroup, and Command.
- **New/Edit/Delete**: Buttons to manage the steps.
- **U/D**: Buttons to move the selected step up or down in the order.
- **OK/Cancel**: Buttons to save changes or cancel.

## Procedure to Add a New Step

### 1. Open Job Properties
   - Navigate to `Job Properties` for the specific job you want to edit.

### 2. Go to Steps Page
   - Click on `Steps` in the navigation pane on the left side.

### 3. Add New Step
   - Click on `New`.
   - Fill out required information such as `StepName`, `Credential`, `TargetGroup`, and `Command`.
   - Click `OK` to save.

### 4. Edit Existing Step (optional)
   - Select an existing step from the list.
   - Click on `Edit`.
   - Modify required fields and click `OK`.

### 5. Delete a Step (optional)
    - Select an existing step from the list.
    - Click on ‘Delete’.
    - Confirm deletion in pop-up window.

## Saving Changes 
After adding, editing or deleting steps ensure you click ‘OK’ at bottom of screen to save all changes made.


# Job Step Management - Step Properties

## Overview
The **Step Properties** screen allows users to manage individual job steps within a job. When a user clicks on a specific step from the steps page of a job, this screen opens. Here are the details of the elements and options available on this screen:

### Interface Elements

1. **Navigation Pane**
   - Located on the left side, it allows users to navigate between different sections: General, Advanced, and Output settings for the selected step.

2. **Step Name**
   - Users can view or edit the name of the selected step here.

3. **Credentials**
   - A dropdown menu allowing users to select or add new credentials for executing this step.

4. **Target Group**
   - Users can assign or change target groups using this dropdown menu.

5. **Command Field**
   - Allows users to input or edit commands associated with this job step.

### Actions
- The `OK` button saves any changes made to the job step properties.
- The `Cancel` button discards any unsaved changes and closes the properties window.

### Progress Indicator
- Located at the bottom left corner, it indicates the processing status when saving changes or executing commands.

# Managing Step Retry Settings

## Overview
The **Advanced** page of the step properties allows users to configure retry settings for optimizing the performance and reliability of their job steps. Below are the options available:

### 1. Step Timeout
- **Description**: The maximum amount of time allocated for a step to complete.
- **Default Value**: 43200 seconds (12 hours).

### 2. Max Parallelism
- **Description**: The maximum number of parallel executions allowed for a step. A value of 0 means null, indicating no limit on parallel executions.
- **Default Value**: 0 (null).

### 3. Retry Attempts
- **Description**: The number of times the system will attempt to retry executing a step in case of failure.
- **Default Value**: 2 attempts.

### 4. Initial Retry Interval
- **Description**: The initial time interval before the first retry attempt is made after a failure.
- **Default Value**: 1 second.

### 5. Maximum Retry Interval
- **Description**: The maximum time interval between retry attempts. Each subsequent retry (after the initial) will double the interval time until this maximum value is reached.
- **Default Value**: 120 seconds.

### 6. Retry Interval Backoff Multiplier 
- **Description**: This multiplier increases the interval between retries exponentially to reach up to the Maximum Retry Interval.
- **Default Value**: 2

## Modifying Retry Settings
1. Navigate to `Step Properties`.
2. Click on `Advanced`.
3. Adjust values as needed using input fields and dropdown menus.
4. Click `OK` to save changes.

Note: These are default values except for Max Parallelism which has a default value of 0 meaning null (unlimited parallel executions allowed).

# Code snippets with line numbers

{: .warning }

In prior versions of the docs, we provided "workarounds" to rendering issues arising from code snippets with line numbers. While these seemed to resolve visual layout issues, they did not resolve core issues with Jekyll generating invalid HTML. See [the detailed explanation](#detailed-error-explanation) for more information.

The default settings for HTML compression are incompatible with the HTML
produced by Jekyll for line numbers from highlighted code
-- both when using Kramdown code fences and when using Liquid highlight tags.

To avoid non-conforming HTML and unsatisfactory layout, HTML compression
can be turned off by using the following configuration option:

{% highlight yaml %}
compress_html:
  ignore:
    envs: all
{% endhighlight %}

When using Kramdown code fences, line numbers are turned on globally by the
following configuration option:

{% highlight yaml %}
kramdown:
  syntax_highlighter_opts:
    block:
      line_numbers: true
{% endhighlight %}

Line numbers can then be suppressed locally using Liquid tags (_without_ the
`linenos` option) instead of fences:

{% highlight yaml %}
{% raw %}{% highlight some_language %}
Some code
{% endhighlight %}{% endraw %}
{% endhighlight %}

## Detailed Error Explanation

Consider this following code snippet, intended to highlight a simple Ruby program:

```
{% raw %}{% highlight ruby linenos %}
def foo
  puts 'foo'
end
{% endhighlight %}{% endraw %}
```

If this is directly placed within a file processed by Jekyll (via Just the Docs, with HTML compression enabled), the following markup will be generated:

```html
<figure class="highlight">><code class="language-ruby" data-lang="ruby"><div class="table-wrapper"><table class="rouge-table"><tbody><tr><td class="gutter gl"><pre class="lineno">1
2
3
</pre><td class="code"><pre><span class="k">def</span> <span class="nf">foo</span>
  <span class="nb">puts</span> <span class="s1">'foo'</span>
<span class="k">end</span>
</pre></figure>
```

This HTML is invalid; in particular, there are two issues:

1. there are many missing closing tags, and a superfluous `>`, which produce visually garbled output
2. a `<table>` is placed within a `<code>` element, which is syntactically invalid HTML (but is often allowed by browsers)

To emphasize this first difference, here is the same markup output, indented by tag:

```html
<figure class="highlight">
  >
  <code class="language-ruby" data-lang="ruby">
    <div class="table-wrapper">
      <table class="rouge-table">
        <tbody>
          <tr>
            <td class="gutter gl">
              <pre class="lineno">
1
2
3
              </pre>
              <td class="code">
                <pre>
<span class="k">def</span>
<span class="nf">foo</span>
<span class="nb">puts</span>
<span class="s1">'foo'</span>
<span class="k">end</span>
                </pre>
</figure>
```

In order, there are missing `</td>`, `</td>`, `</tr>`, `</tbody>`, `</table>`, `</div>`, and `</code>` tags. As a result, the following elements of the page - including the site footer - become visually garbled as browsers attempt to recover gracefully.

Prior workarounds we suggested (such as [Dmitry Hrabrov's in `jekyll-compress-html`#71](https://github.com/penibelst/jekyll-compress-html/issues/71#issuecomment-188144901)) resolve the missing tag problem. However, they still place a `<table>` within a `<code>` element. The HTML spec normatively states that `<code>` elements should only contain "[phrasing content](https://html.spec.whatwg.org/multipage/dom.html#phrasing-content-2)", which does not include `<table>` ([spec ref](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-code-element)). To avoid incorrectly rendered HTML, the previously-suggested workaround using the current version of `_includes/fix_linenos.html` should _not_ be used!
