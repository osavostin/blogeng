---
title: Markdown
summary: A small guide
date: 2025-04-11
authors:
  - admin
tags:
  - Second Brain
  - Markdown
image:
---

Introduction

GitHub is a widely used platform for version control and collaborative development, but it’s also an excellent platform for documenting, writing, and formatting content using Markdown. Whether you're writing README files, project documentation, or contributing to a wiki page, understanding how to format text on GitHub will improve the readability and professionalism of your work.

In this article, you'll learn how to write and format on GitHub using Markdown, along with some useful tips and tools to enhance your writing.

About Markdown

What is Markdown?Markdown is a lightweight markup language that allows you to format text in a simple and readable way. It is widely used on GitHub for writing README files, issues, pull request descriptions, and more. Markdown syntax is intuitive and readable even in raw form, making it ideal for collaborative writing and documentation.

Markdown files usually use the .md file extension.

Basic Markdown Formatting

Here are some common Markdown formatting methods you can use in your GitHub repositories:

HeadingsHeadings are created using the # symbol followed by a space. The number of # symbols indicates the heading level (from h1 to h6).

# Heading 1

## Heading 2

### Heading 3

EmphasisYou can italicize or bold text using * or _ for italics, and ** or __ for bold.

italic or italic

bold or bold

ListsIn Markdown, you can easily create ordered and unordered lists:

Unordered list: use *, -, or +

Ordered list: use numbers followed by a period

Example:

Item 1

Item 2

Item 3

First item

Second item

Links and ImagesTo insert a link, use the following syntax:

[Link text](URL)

To insert an image, use the same syntax with an exclamation mark (!) at the beginning:

![Alt text](ImageURL)

Code and Syntax Highlighting

GitHub Markdown supports inline code and code blocks. Syntax highlighting is available for most programming languages.

Inline code: Use backticks to format inline code.Example: inline code

Code blocks: Use triple backticks (```) and specify the language.

Example:

```javascript
const hello = 'Hello, world!';
console.log(hello);
```

This formatting helps make your code readable and understandable, especially when collaborating with others.

Blockquotes and Horizontal Lines

Blockquotes: Use > to create blockquotes. Useful for quoting text or highlighting sections.

Example:

This is a blockquote.

Horizontal lines: Use three or more hyphens (---), asterisks (***), or underscores (___).

Example:

---

TablesCreating tables in Markdown is easy. Use vertical bars (|) to separate columns and hyphens (-) to define headers.

Example:

| Header 1 | Header 2 |
| -------- | -------- |
| Cell 1   | Cell 2   |
| Cell 3   | Cell 4   |

Tables are useful for organizing data clearly, especially in documentation.

Task ListsTask lists let you create checklists in issues, pull requests, and comments.

Example:



Task Lists

Task lists are perfect for tracking progress on issues or project tasks.

GitHub Flavored Markdown (GFM)GitHub Flavored Markdown extends the standard Markdown syntax with additional formatting options, including:

Task lists (as shown above)

Mentions: You can tag collaborators using @ followed by their username (e.g., @octocat)

Strikethrough: Use ~~ to strike through text.Example:This is strikethrough text.

Working with README Files

README files are one of the most important aspects of a GitHub repository. They provide an overview of the project and typically include installation instructions, usage examples, and contact information.

Here’s a simple example of a README file.

Writing Wiki Pages

GitHub wikis use the same Markdown syntax and are ideal for organizing documentation for large projects. Each wiki page can focus on a specific topic, and you can link pages together to create detailed documentation.

Conclusion

Writing and formatting on GitHub using Markdown is a simple yet powerful way to create clear and professional documentation for your projects. Whether you're writing a README, an issue, or documentation pages, understanding Markdown basics helps you communicate effectively.

By using the tools and tips in this guide, you can:

Create well-structured documentation

Improve collaboration by clarifying issues and pull requests

Maintain a clean and professional presence for your project on GitHub

Being proficient with Markdown on GitHub is essential for any developer who wants to contribute to or maintain open-source projects.
