# Quick Guide to Editing the MES CoP Website

This page uses the **Markdown** language and a small amount of **HTML**. You do **not** need to know how to write code to make most updates. Most changes involve editing text or copying an existing table row.

## Common Notation You'll See

### Comments

```html
<!-- This is a comment -->
```

* Comments are **only visible while editing** the file.
* They **do not appear** on the published webpage.
* Comments are used to provide instructions or reminders for future editors.

---

### Markdown Headings

Headings organize the page into sections.

```markdown
# Main Heading
## Section Heading
### Subsection
#### Smaller Subsection
```

The more `#` symbols, the smaller the heading.

Example:

```markdown
# CMS MES Community of Practice
## Upcoming CoP Sessions
### Registration Information
```

---

### Regular Text

Normal paragraphs are written as plain text.

```markdown
This is regular text that appears on the webpage.
```

Leave a blank line between paragraphs for proper spacing.

---

### Bullet Lists

Use an asterisk (`*`) to create bullet points.

```markdown
* First item
* Second item
* Third item
```

This displays as:

* First item
* Second item
* Third item

---

### Links

A link allows users to open another webpage or document.

HTML example:

```html
<a href="https://example.com">Register Here</a>
```

* The text between `>` and `</a>` is what visitors click.
* The URL inside `href=""` is where the link goes.

---

## HTML Tables

Tables are used for the **Upcoming CoP Sessions** and **Past CoP Sessions**.

### Table

```html
<table>
```

Starts a table.

```html
</table>
```

Ends a table.

---

### Table Row

```html
<tr>
```

Begins one row.

```html
</tr>
```

Ends that row.

Think of one `<tr>` as one complete session. If the published webpage looks strange, as if code is like ```</table>``` or similar is appearing, it's often because there's a missing ``` </tr> ``` somewhere on the page. 

---

### Table Cell

```html
<td>
```

Starts one cell (or column) within a row.

```html
</td>
```

Ends that cell.

For example:

| Date | Topic | Registration |
| ---- | ----- | ------------ |

contains three `<td>` cells.

---

### Table Headings

```html
<th>Date</th>
```

Creates the header row at the top of the table.

You generally won't need to edit these.

---

### Line Break

```html
<br>
```

Creates a new line without starting a new paragraph.

It is commonly used when listing multiple links in one table cell.

---

## Common Editing Tasks

### Add a New Session

1. Copy an existing `<tr> ... </tr>` block.
2. Paste it where you want the new session.
3. Replace the date, topic, and links.

---

### Update a Session

Edit only the text or links between the tags.

For example:

```html
<td>Agile Oversight Model</td>
```

can become

```html
<td>Project Status Reports</td>
```

---

### Delete a Session

Delete one complete row:

```html
<tr>
...
</tr>
```

Be sure to delete both the opening `<tr>` and closing `</tr>` tags.

---

## Tips

* Edit only the text you intend to change.
* If you're unsure, copy an existing row and modify it rather than creating one from scratch.
* Leave comments (`<!-- -->`) in place—they are there to help editors.
* If something doesn't look right after editing, check that every opening tag (such as `<tr>` or `<td>`) has a matching closing tag (`</tr>` or `</td>`).
* Saving frequently makes it easier to identify and fix mistakes.

---

## Detailed Instructions: How to update "Upcoming CoP sessions" 

<!--
=========================================================
HOW TO UPDATE THIS TABLE
=========================================================

You will usually only need to do ONE of these things:

1. ADD A NEW SESSION
   - Copy one complete <tr> ... </tr> block.
   - Paste it below the last session.
   - Replace the date, topic, and registration link.

2. UPDATE A SESSION
   - Edit the text between the <td> and </td> tags.
   - Update the registration link if needed.

3. DELETE A SESSION
   - Delete one complete <tr> ... </tr> block.

TIP:
Each <tr> represents ONE ROW in the table.
Each <td> represents ONE CELL (column) in that row.

=========================================================
-->

<table>

  <!-- Table headings. Usually you never need to change these. -->
  <thead>
    <tr>
      <th>Date</th>
      <th>Topics</th>
      <th>Registration Link</th>
    </tr>
  </thead>

  <tbody>

    <!--
    =========================================================
    TEMPLATE ROW

    Copy everything from <tr> to </tr> below
    to create a new session.

    Replace:
    - Date
    - Topic
    - Registration URL
    =========================================================
    -->

    <tr> <!-- This is a comment, the browser will ignore this completely -->NOTE: Select everything from here to Line 72 
      <td>
        Wednesday, Month DD, YYYY | 2:00 PM - 3:00 PM EDT | Online event
      </td>

      <td>
        Example Topic<br>
      </td>

      <td>
        <a href="https://example.com">
          Register Here
        </a><br>
      </td>
    </tr> // // NOTE: Select everything from here from Line 56. Copy and past this immediately before a <tr> or immediately after </td>

    <!-- CURRENT SESSION -->

    <tr>
      <td>
        Wednesday, July 29, 2026 | 2:00 PM - 3:00 PM EDT | Online event
      </td>

      <td>
        Agile Oversight Model<br>
      </td>

      <td>
        <a href="https://events.gcc.teams.microsoft.com/event/b40cc45a-c0a8-4a35-a49e-6def96a8f259@fbdcedc1-70a9-414b-bfa5-c3063fc3395e">
          Register Here
        </a><br>
      </td>
    </tr>

  </tbody>
</table>

---

## Detailed Instructions: How to update "Past CoP sessions"

<!--
=========================================================
HOW TO UPDATE THIS TABLE
=========================================================

When a session is over:

1. Copy the entire row from the Upcoming Sessions table.
2. Paste it at the TOP of this table.
3. Change the last column:
   Remove "Register Here"
   Add links to:
      • Meeting Recording
      • Meeting Transcript (if available)
      • Slide Deck(s)

To remove a session, delete one complete
<tr> ... </tr> block.

=========================================================
-->

<table>

  <!-- These column titles rarely change -->
  <thead>
    <tr>
      <th>Date</th>
      <th>Topics</th>
      <th>Documents</th>
    </tr>
  </thead>

  <tbody>

    <!--
    =========================================================
    TEMPLATE ROW

    Copy this entire row when adding a completed session.
    Replace all placeholder text with the new session's
    information.
    =========================================================
    -->

    <tr>

      <!-- Date column -->
      <td>
        Wednesday, Month DD, YYYY | 2:00 PM - 3:00 PM EDT | Online event
      </td>

      <!-- Topic column -->
      <td>
        Example Topic<br>
      </td>

      <!-- Documents column -->
      <td>

        <a href="https://example.com">
          Meeting Recording
        </a><br>

        <a href="assets/example-transcript.docx"
           target="_blank"
           rel="noopener noreferrer">
          Meeting Transcript
        </a><br>

        <a href="assets/example-slide-deck.pptx"
           target="_blank"
           rel="noopener noreferrer">
          Slide Deck
        </a><br>

      </td>

    </tr>

    <!-- Existing sessions go below this line -->

    <!-- March 2026 -->
    <tr>
      ...
    </tr>

    <!-- April 2026 -->
    <tr>
      ...
    </tr>

    <!-- May 2026 -->
    <tr>
      ...
    </tr>

    <!-- June 2026 -->
    <tr>
      ...
    </tr>

  </tbody>

</table>
