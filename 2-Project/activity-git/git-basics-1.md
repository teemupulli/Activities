# Lab: Getting Started with Git: Basic Operations

In this lab, you'll get hands-on experience with the fundamental Git commands.

**Step 1:Setting Up Your Environment**

Before you can start using Git, you need to install it and configure some basic settings. Follow these steps to get Git up and running on your system.

1. Install Git

- Windows: You can easily install `Git` in Windows by using the installer found at [https://git-scm.com/](https://git-scm.com/).

Once you've downloaded one of the "Git for Windows Setup" distributions (either
32-bit or more likely 64-bit) you can launch the installer and accept all the
defaults.

- Mac: Mac comes with some tools by default. Git is one that you want to make sure is up
to date so you can run the following in your terminal.

```shell
xcode-select --install
```
   
2. Configure Git

Once you have installed git, configure the information that gets logged for each
of your commits by updating the default (global) credentials that git uses. (You
could overwrite these credentials temporarily per local repo. While that
shouldn't be necessary, it is helpful to know that it is an option.) You will also want to set the default branch to `main`.

In your terminal, run

```shell
git config --global user.name "Your Name"
git config --global user.email "Your Email"
git config --global init.defaultBranch main
```

Check that your name and email have been set up correctly by using the following commands:

```shell
git config user.name
git config user.email
```

You should see your name and email address returned. Repeat this step if there
are any errors.

3. **Create a New Project Directory:**
Open your terminal and navigate to a directory where you want to create your project. Create a new folder for your project using:
```sh
mkdir git-basics-lab
cd git-basics-lab
```

**Step 2: Initializing a Git Repository**

1. **Initialize Git Repository:**
Run the following command to initialize a new Git repository in your project folder:
```sh
git init
```

**Step 3: Making and Committing Changes**

1. **Create Files:**
Create a new file named `README.md` in your project folder. Open the file in a text editor and add some content, e.g. "Welcome to My Git Basics Lab."

2. **Stage Changes:**
Use the following command to stage the changes you've made:
```sh
git add README.md
```

3. **Commit Changes:**
Commit the staged changes with a descriptive message using the following command:
```sh
git commit -m "Initial commit: Added README.md"
```

**Step 4: Basic Git Operations**

1. **View Repository Status:**
Use the following command to see the current status of your repository:
```sh
git status
```

2. **View Commit History:**
View the commit history to see your commit using:
```sh
git log
```

**Step 5: Making and Committing More Changes**

1. **Modify `README.md`:**
Open `README.md` again in a text editor and make some changes to the content.

2. **Stage and Commit Changes:**
Repeat the steps to stage and commit the changes you've made to `README.md`.

**Step 6: Create a New File and Commit**

1. **Create a New File:**
Create a new file named `journal.md` in your project folder. 

2. Add a Title

Use a single `#` to create a primary title for your journal entry:

```markdown
# My Reflection Journal - [Date]
```

Replace `[Date]` with the specific date of your reflection.

3. Subheadings

Use `##`, `###`, and so on, to create subheadings for different sections or topics in your journal:

```markdown
## Personal Growth
### Achievements
### Challenges
## Learning
### New Concepts
### Insights
```

4. Lists

You can create both ordered (numbered) and unordered (bulleted) lists.

Unordered (bulleted) list:

```markdown
- Item 1
- Item 2
- Item 3
```

Ordered (numbered) list:

```markdown
1. First Item
2. Second Item
3. Third Item
```

5. Emphasize Text

Use `*` or `_` to emphasize text. A single `*` or `_` will italicize text, and a double `**` or `__` will make it bold:

```markdown
*Italic Text*
**Bold Text**
```

6. Links

Create links to external websites or resources using square brackets for the link text and parentheses for the URL:

```markdown
[OpenAI](https://www.openai.com/)
```

7.  Images

Embed images using an exclamation mark followed by square brackets for alt text and parentheses for the image URL:

```markdown
![Alt Text Hedy Lamarr](https://i.imgur.com/yXOvdOSs.jpg)
```

8. Blockquotes

Use `>` to create blockquotes for adding quotations or references:

```markdown
> "The only source of knowledge is experience." - Albert Einstein
```

9. Code Blocks

Use triple backticks (```) to create code blocks or inline code:

```markdown
```javascript
console.log("Hello, World!");
```

Inline code: `const variable = 42;`

10. Horizontal Lines

Add horizontal lines to separate sections with `---` or `___`:

```markdown
---
```

11. Line Breaks

Use two spaces at the end of a line to create a line break.

12. Save and Review

After adding your content, save the file, and review it. Make sure it's formatted as you desire and that it effectively captures your reflections.

13. Stage and Commit:
Stage and commit the new file `journal.md` with an appropriate message.

**Summary:**

In this lab, you got hands-on experience with Git's core commands: `init` to initialize a Git repository, and `add` and `commit` to track and save changes. You also learned how to view the status of your repository and the commit history. This foundational knowledge will serve as the basis for more advanced Git workflows and collaborative development. 