---
layout: default
title: Manage target group
parent: Documentation
has_children: true
nav_order: 9
---
# Creating Target Groups and Adding Targets

## Overview
The **Create Target Group** screen allows users to create a new target group. Once the target group is created, users can add specific targets (databases) where jobs will be executed.

## Steps to Create a Target Group and Add Targets

1. **Navigate to the Create Target Group Screen**
   - Click on "Create Target Group" to open this interface.

2. **Enter the Target Group Name**
   - In the "Target group name" field, enter a unique and descriptive name for your new target group.

3. **Create the Target Group**
   - Click on the “Create target group” button after entering the desired name.
   - The system will validate if a similar named group exists or not, ensuring uniqueness.

4. **Add Targets (Post-Creation)**
    - Once the target group is created, options become available for adding targets.
    - Click on “Add target” and follow subsequent prompts to add databases where jobs will be executed.

## Fields and Options

- **Target group name:** A text field for entering the name of your new target group.
- **Permission script:** An optional feature allowing users to attach permission scripts if necessary.
- **Add target:** This option becomes available post creation of a target group, allowing users to add specific targets or databases.

### Closing Interface
Click on “Close” button at bottom right corner of screen to exit out of this interface and return back to previous menu or dashboard.


# Callouts
{: .d-inline-block }

New (v0.4.0)
{: .label .label-green }

Markdown does not include support for callouts. However, you can style text as a callout using a Markdown extension supported by kramdown: [*block IALs*](https://kramdown.gettalong.org/quickref.html#block-attributes).

Common kinds of callouts include `highlight`, `important`, `new`, `note`, and `warning`.

{: .warning }
These callout names are *not* pre-defined by the theme: you need to define your own names.

When you have [configured]({% link docs/installation.md %}#callouts) the  `color` and (optional) `title` for a callout, you can apply it to a paragraph, or to a block quote with several paragraphs, as illustrated below.[^postfix]

[^postfix]:
    You can put the callout markup either before or after its content.

#### An untitled callout
{: .no_toc }

```markdown
{: .highlight }
A paragraph
```

{: .highlight }
A paragraph


#### A single paragraph callout
{: .no_toc }

```markdown
{: .note }
A paragraph
```

{: .note }
A paragraph

```markdown
{: .note-title }
> My note title
>
> A paragraph with a custom title callout
```

{: .note-title }
> My note title
>
> A paragraph with a custom title callout

#### A multi-paragraph callout
{: .no_toc }

```markdown
{: .important }
> A paragraph
>
> Another paragraph
>
> The last paragraph
```

{: .important }
> A paragraph
>
> Another paragraph
>
> The last paragraph

```markdown
{: .important-title }
> My important title
>
> A paragraph
>
> Another paragraph
>
> The last paragraph
```

{: .important-title }
> My important title
>
> A paragraph
>
> Another paragraph
>
> The last paragraph

#### An indented callout
{: .no_toc }

```markdown
> {: .highlight }
  A paragraph
```

> {: .highlight }
  A paragraph

#### Indented multi-paragraph callouts
{: .no_toc }

```markdown
> {: .new }
> > A paragraph
> >
> > Another paragraph
> >
> > The last paragraph
```

> {: .new }
> > A paragraph
> >
> > Another paragraph
> >
> > The last paragraph


#### Nested callouts
{: .no_toc }

```markdown
{: .important }
> {: .warning }
> A paragraph
```

{: .important }
> {: .warning }
> A paragraph

#### Opaque background
{: .no_toc }

```markdown
{: .important }
> {: .opaque }
> <div markdown="block">
> {: .warning }
> A paragraph
> </div>
```

{: .important }
> {: .opaque }
> <div markdown="block">
> {: .warning }
> A paragraph
> </div>
