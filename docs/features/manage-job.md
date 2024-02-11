---
layout: default
title: Manage job
parent: Documentation
has_children: true
nav_order: 2
---

# Manage a job in Azure Elastic Jobs
{: .no_toc }
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Create or alter the job

Follow these steps to create a new job using the **Azure Elastic Job Agent** interface:

1. **Navigation**
   - On the left panel, select "New Job" to open the job creation window.

2. **General Information**
   - **Name:** Enter the name of your job in the 'Name' field.
   - **Description:** Provide a detailed description of your job in the 'Description' field.

3. **Job Execution Details**
   - **Last Run Outcome:** This field will display the outcome of the last run once the job has been executed.
   - **Last Executed:** Indicates when this particular job was last executed.
     
4. **Script & Help Options**
   - Click on “Script” if you need to view or edit scripts associated with this job.
   - Click on “Help” for assistance and documentation related to this interface.

5. **Progress Indicator**
   - Monitor real-time progress at the bottom left corner under "Progress."

6. **Save or Cancel**
   - Click “OK” to save and create your new job.
   - Click “Cancel” if you wish not to proceed with creating this new job.

### Note:
Ensure all required fields are filled out before clicking "OK" to avoid errors and ensure smooth creation of your new Azure elastic jobs.

---

## Start job
 **Steps to start an elastic job**
   - On the left panel of the landing screen, right click on the job under 'Jobs' tree view.
   - From the menu items, click 'Start job' button.

## Stop job
 **Steps to stop an elastic job**
   - On the left panel of the landing screen, right click on the job under 'Jobs' tree view.
   - From the menu items, click 'Stop job' button.

## Enable/Disable job
 **Steps to enable/disable an elastic job**
   - On the left panel of the landing screen, right click on the job under 'Jobs' tree view.
   - From the menu items, click 'Enable'/'Disable' button. 

Note: Enable or Disable button in the menu list will apoear deoending on the current activation status of the job.

## View history

### Links that look like buttons

<div class="code-example" markdown="1">
[Link button](https://just-the-docs.com){: .btn }

[Link button](https://just-the-docs.com){: .btn .btn-purple }
[Link button](https://just-the-docs.com){: .btn .btn-blue }
[Link button](https://just-the-docs.com){: .btn .btn-green }

[Link button](https://just-the-docs.com){: .btn .btn-outline }
</div>
```markdown
[Link button](https://just-the-docs.com){: .btn }

[Link button](https://just-the-docs.com){: .btn .btn-purple }
[Link button](https://just-the-docs.com){: .btn .btn-blue }
[Link button](https://just-the-docs.com){: .btn .btn-green }

[Link button](https://just-the-docs.com){: .btn .btn-outline }
```

### Button element

GitHub Flavored Markdown does not support the `button` element, so you'll have to use inline HTML for this:

<div class="code-example">
<button type="button" name="button" class="btn">Button element</button>
</div>
```html
<button type="button" name="button" class="btn">Button element</button>
```

---

## Using utilities with buttons

### Button size

Wrap the button in a container that uses the [font-size utility classes]({% link docs/utilities/typography.md %}) to scale buttons:

<div class="code-example" markdown="1">
<span class="fs-6">
[Big ass button](https://just-the-docs.com){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](https://just-the-docs.com){: .btn }
</span>
</div>
```markdown
<span class="fs-8">
[Link button](https://just-the-docs.com){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](https://just-the-docs.com){: .btn }
</span>
```

### Spacing between buttons

Use the [margin utility classes]({% link docs/utilities/layout.md %}#spacing) to add spacing between two buttons in the same block.

<div class="code-example" markdown="1">
[Button with space](https://just-the-docs.com){: .btn .btn-purple .mr-2 }
[Button](https://just-the-docs.com){: .btn .btn-blue }

[Button with more space](https://just-the-docs.com){: .btn .btn-green .mr-4 }
[Button](https://just-the-docs.com){: .btn .btn-blue }
</div>
```markdown
[Button with space](https://just-the-docs.com){: .btn .btn-purple .mr-2 }
[Button](https://just-the-docs.com){: .btn .btn-blue }

[Button with more space](https://just-the-docs.com){: .btn .btn-green .mr-4 }
[Button](https://just-the-docs.com){: .btn .btn-blue }
```
