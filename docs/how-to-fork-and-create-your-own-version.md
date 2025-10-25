# How to fork this repo and make your own version
A friendly step-by-step guide for people who don't often use GitHub. This explains how to copy (fork) the repository, make changes, and publish your own version. It includes both web (GUI) steps and command-line examples.

---

## Quick summary
- If you want your own copy on GitHub: Fork the repo → Clone it locally → Create a branch → Make changes → Push → (Optional) Open a pull request upstream.
- If you don't use Git: Download the ZIP → Make edits locally → Create a new repository and upload your files.
- Use GitHub Desktop or VS Code for an easier GUI workflow.

---

## 1) Fork the repository (make your own copy on GitHub)
1. Go to this repo on GitHub: https://github.com/all-uto/time-trickster  
2. In the upper-right corner, click the "Fork" button.  
3. Choose your personal account (or an organization) to own the fork.  
Now you have a copy at https://github.com/YOUR_USERNAME/time-trickster.

Why fork? Forking keeps a link to the original project (upstream) so you can propose changes back later, or just keep your own independent copy.

---

## 2) Clone your fork to your computer
You can use the Git command line, GitHub Desktop, or VS Code.

Command line:
1. Open a terminal.
2. Run:
   - git clone git@github.com:YOUR_USERNAME/time-trickster.git
   - cd time-trickster

If you prefer HTTPS:
   - git clone https://github.com/YOUR_USERNAME/time-trickster.git

GitHub Desktop:
1. File → Clone repository → Your GitHub.com → select your fork → Clone.

VS Code:
1. Use "Clone Repository" from the Welcome page or Command Palette (Ctrl/Cmd+Shift+P → Git: Clone).

---

## 3) Create a branch for your changes
Always make changes on a branch (not directly on main).

Command line:
- git checkout -b my-changes
Replace `my-changes` with a short name (e.g., rename-assets, update-readme).

In GitHub Desktop or VS Code you can create a new branch with a button/menu.

---

## 4) Make edits
- Edit files in your editor (VS Code recommended).
- Add or replace assets under the `assets/` folder.
- Update documentation under `docs/` or `README.md`.

Helpful tips:
- Keep each change focused and small (one topic per branch).
- Write a short commit message summarizing the change.

---

## 5) Commit and push your branch
Command line:
- git add .
- git commit -m "Short description: what & why"
- git push --set-upstream origin my-changes

GitHub Desktop & VS Code:
- Use the Commit UI, then Push.

After pushing, your branch will appear on your GitHub fork.

---

## 6) Publish (optional): Open a Pull Request (PR)
If you want the original project to adopt your changes:
1. On GitHub, go to your fork and open the branch.
2. Click "Pull request" → "Compare & pull request".
3. Add a description and submit it.

If you just want your own version, you don't need to open a PR.

---

## 7) If you don't use Git at all (download ZIP method)
1. On the original repo page, click "Code" → "Download ZIP".
2. Unzip locally and make your changes.
3. Create a new repository on GitHub (click + → New repository).
4. Upload files using the web UI (drag-and-drop) OR initialize the new repo locally and push.

This method is simple, but you'll lose the fork link to the original repo and history (no easy PRs).

---

## 8) Rename, license, and publishing considerations
- Rename: change repository name in Settings → Repository name (or rename files/README to reflect a new project name).
- License: this repo has a LICENSE file (CC0). You may relicense your *own* additions, but be cautious about relicensing third‑party content included in the repo.
- Attribution: even when license allows reuse, crediting the original project is good community practice.

---

## 9) Make it your own — encouragement and practical tips
We encourage you to make a version that fits your group's vision. Forking is designed for exactly this: take the parts that inspire you, change the rest, and create something new.

Ideas and steps to make the fork truly yours:
- Rename the project and update the README to explain your vision (what's different, who it's for).
- Add a short "About this variant" section near the top of your README, e.g.:

  "This is MY_FORK_NAME — a community-driven variant of all-uto/time-trickster focused on playful narrative prompts and wearable cosplay guides. It started as a fork of all-uto/time-trickster; we’ve changed assets and prompts to better reflect our theme."

- Create a VISION.md or ROADMAP.md that explains your goals, style guide, and what contributions you're looking for.
- Update the LICENSE if you want a different license for your additions (but keep the original attribution where needed). If you relicense, clearly state which parts are under which license.
- Curate the assets: replace or add images, patterns, and prompts that match your vision.
- Set community expectations: update CONTRIBUTING.md and CODE_OF_CONDUCT.md to match how you want contributors to behave.

Good to know about relicensing and third-party content:
- You can license your own new content however you like, but you cannot change the original license of content that came from others unless you have the rights to do so. Keep a clear "Files and Licenses" section in your README listing any exceptions.

---

## 10) Example README intro for a personal fork
Copy and paste this near the top of your README and edit it:

> # MY_FORK_NAME
> 
> MY_FORK_NAME is a community variant of the time-trickster project, focused on X, Y, and Z. This repository began as a fork of all-uto/time-trickster — we’ve adapted the assets and prompts so that the project reflects our group’s aesthetic. See LICENSE and the Files and Licenses section for details about what’s original and what we changed.

---

## 11) Example commands (quick copy/paste)
Replace YOUR_USERNAME and branch names before running.

Clone:
- git clone git@github.com:YOUR_USERNAME/time-trickster.git
- cd time-trickster

Create branch & commit:
- git checkout -b update-instructions
- git add docs/how-to-fork-and-create-your-own-version.md
- git commit -m "Add beginner instructions for forking and contributing"
- git push --set-upstream origin update-instructions

Open PR:
- (on GitHub) Click Compare & pull request

---

## 12) Suggested commit message styles
- chore: update wording in README
- docs: add beginner guide for forking
- feat: add new character sprite and README example
- fix: correct asset attribution

These prefixes help readers quickly know what changed.

---

## 13) Common issues & troubleshooting
- Permission denied (SSH): you don’t have SSH keys set up. Either set them up (https://docs.github.com/en/authentication/connecting-to-github-with-ssh) or use the HTTPS clone URL.
- “remote: Repository not found”: check the clone URL and your username.
- “Failed to push”: you may need to set upstream (see git push --set-upstream ...).
- Conflicts when merging: pull the latest changes from upstream and resolve conflicts in your editor before pushing.

To pull upstream changes into your fork:
1. Add upstream (one time only):
   - git remote add upstream https://github.com/all-uto/time-trickster.git
2. Fetch and merge:
   - git fetch upstream
   - git checkout main
   - git merge upstream/main
   - git push origin main

---

## 14) Using GitHub Desktop or VS Code (easier GUI)
- GitHub Desktop: clone your fork, use the Branch menu to create branches, commit, and push with buttons.
- VS Code: built-in Source Control pane, Branch indicator in the lower-left, integrated terminals, and GitLens extensions available.

If you want, I can add a short GIF or screenshots later showing the GUI steps.

---

## 15) Checklist before publishing your forked project
- [ ] README updated to reflect your project name/goal
- [ ] License chosen and documented
- [ ] Asset attributions verified
- [ ] Example usage included (how to use prompts/assets)
- [ ] Contact info or contributing guidance added

---

## 16) Need help or want me to do it for you?
If you'd like, I can:
- Create a pre-configured fork & branch (I can prepare instructions you can run).
- Make the initial edits and open a PR in your fork.
- Add screenshots or a short screencast showing the steps.

If you want me to include step-by-step code snippets for a specific environment (Windows, macOS, or Linux), say which one and I’ll add them.

---

## 17) Useful links
- GitHub: Fork a repo — https://docs.github.com/en/get-started/quickstart/fork-a-repo  
- GitHub: Create a pull request — https://docs.github.com/en/pulls


Thanks — this file is aimed at people who are new to GitHub. If you'd like, I can:
- Add screenshots,
- Add a short video/screencast script,
- Create a printable one-page cheat sheet for your group.

Tell me which and I’ll add it next.
