---
layout: default
title: Manage step
parent: Manage job
grand_parent: Documentation
permalink: /docs/featurees/manage-job/manage-step/
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
