Here is the project plan formatted as a ready-to-use Markdown file. You can copy this code, save it as `README.md` or `PROJECT_PLAN.md`, and share it with your learners.

````markdown
# 🚀 Version Control Practice Project: The DevTeam Dashboard

## Project Overview
**Goal:** Build a collaborative "Team Dashboard" where 8 developers implement individual features into a single shared codebase.
**Focus:** Practicing branching, committing, pull requests, code reviews, and **resolving merge conflicts**.
**Tech Stack:** HTML5, CSS3, Vanilla JavaScript.

---

## 📂 Repository Structure
The repository should be set up initially as follows:

```text
/
├── index.html       (The main skeleton)
├── css/
│   └── style.css    (Global styles & CSS variables)
├── js/
│   └── app.js       (Global scripts)
└── assets/          (Images/Icons)
````

-----

## 📜 The Workflow (Rules of Engagement)

1.  **No Direct Pushing to Main:** Everyone must create a feature branch (e.g., `feature/dark-mode`, `feature/contact-form`).
2.  **The "Conflict Trap":** To ensure you practice resolving conflicts:
      * Every feature must be linked in the main **Navigation Bar** in `index.html`.
      * Every feature should utilize the CSS variables defined in `style.css`.
3.  **Pull Requests:** When a feature is done, open a Pull Request (PR) against `main`. It must be reviewed by at least one other team member.

-----

## 👥 Team Roles & Assignments

Each learner has a specific role. Assign these before starting.

### 1\. The Architect (Repo Owner)

  * **Responsibility:** Initialize the Git repo, add collaborators, and create the initial file structure.
  * **Feature:** Build the **Responsive Navigation Bar**.
  * **Conflict Potential:** High. You control the `index.html` skeleton others depend on.

### 2\. The Stylist (Themes)

  * **Responsibility:** Define global CSS variables in `:root` (colors, fonts).
  * **Feature:** Create a **Dark/Light Mode Toggle**. Use JS to toggle a class on the `<body>` that changes the CSS variables.
  * **Conflict Potential:** High. You are editing `style.css` which everyone uses.

### 3\. The Task Master (Productivity)

  * **Feature:** A **To-Do List Widget**.
  * **Requirements:** Input field, "Add" button, and a list `<ul>`.
  * **JS Logic:** Add items to the DOM dynamically. Add a "delete" button for each item.

### 4\. The Timekeeper (Utilities)

  * **Feature:** A live **Digital Clock & Date Widget**.
  * **Requirements:** Must update every second.
  * **JS Logic:** Use `setInterval()` and the `Date` object.
  * **CSS:** Style it to look like a digital alarm clock.

### 5\. The Gamer (Entertainment)

  * **Feature:** A **Number Guessing Game** (1-100).
  * **Requirements:** Input field for guess, submit button, and a result text area.
  * **JS Logic:** Generate random number, compare input, return "Too High", "Too Low", or "Correct".

### 6\. The Connector (Communication)

  * **Feature:** A **Contact Admin Form**.
  * **Requirements:** Fields for Name, Email, and Message.
  * **JS Logic:** Validate that the email contains an "@" and fields are not empty. Show an alert on success. **Prevent** actual form submission (page reload) using `e.preventDefault()`.

### 7\. The Wise One (Content)

  * **Feature:** A **Random Quote Generator**.
  * **Requirements:** A card displaying a quote and a "New Quote" button.
  * **JS Logic:** Store an array of objects `[{text: "", author: ""}]` and pick a random index on click.

### 8\. The Profiler (Team Section)

  * **Feature:** A **"Meet the Team" Grid**.
  * **Requirements:** A responsive grid displaying 8 profile cards (use placeholders).
  * **JS Logic:** Click a card to open a "Modal" (popup) with more details about that user.

-----

## 🚦 Execution Steps (For the Team)

### Phase 1: Setup (15 Mins)

  - [ ] **Architect:** Create repo, push empty skeleton, add team as collaborators.
  - [ ] **Team:** Clone the repo locally. `git clone <url>`

### Phase 2: Development (1 Hour)

  - [ ] **Team:** Create your branch. `git checkout -b feature/my-feature`
  - [ ] **Team:** Build your feature.
  - [ ] **Team:** **CRITICAL:** Add a link to your feature in the `<nav>` tag in `index.html`. (This will cause the conflicts we want\!).

### Phase 3: The Merge Party (Conflict Resolution)

  - [ ] **Architect:** Merge your Navigation bar changes to `main` first.
  - [ ] **Stylist:** Open a PR. Team reviews. Merge.
  - [ ] **Task Master:** Open a PR. **STOP.** You likely have a merge conflict in `index.html` or `style.css`.
    1.  Pull the latest `main` into your branch: `git pull origin main`
    2.  Fix the conflict in your editor (decide which code to keep).
    3.  Commit the fix.
    4.  Update your PR.
  - [ ] **Rest of Team:** Repeat the process one by one.

<!-- end list -->

```
