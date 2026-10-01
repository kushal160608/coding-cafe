# Lab 4 Notes

## Q1
`--global` saves the setting in my home folder (~/.gitconfig), so it applies to every repository on my computer. Without it, Git only saves the setting for the current repository (in .git/config), so it would apply to that one project only, and it would fail outside a repo.

## Q2
`ls -a` showed a hidden `.git` folder, which `ls` doesn't show because its name starts with a dot. It holds everything Git needs for the repository: the saved commits and file contents (objects), the branches and tags (refs), HEAD, and the repo's config.

## Q3
Git offered to track about 3 entries: README.md, .gitignore and the week02/ folder. Nothing in the list was something I didn't write, because my coding-cafe folder has no .venv folder.

## Q4
Nothing noticeable disappeared, because my first status was already short and had no .venv/ or other junk files in it. The only change was that .gitignore itself appeared as a new untracked file. The ignore rules would hide .venv/, __pycache__/, *.pyc and .DS_Store if they were present.

## Q5
`.gitignore` should be committed. It is part of the project, so committing it means anyone who clones the repo gets the same ignore rules, and the rules are kept in the history. If it were ignored, the rules would exist only on my laptop.

## Q6
`README.md` moved from "Untracked files" to "Changes to be committed". In the three-places model it moved from the working directory to the staging area, and it is not yet in the repository.

## Q7
Git printed `[master (root-commit) 1e04104] Lab work so far` followed by "4 files changed, 72 insertions(+)", plus a list of the created files. It said 4 files changed because all four files were being saved for the first time.
(Check this against your own output. Note that it says `main` if you renamed the branch before committing.)

## Q8
The first seven characters (`1e04104` in my case) are the short commit hash, an abbreviation of the commit's full unique ID. It is used to identify and refer to one specific commit, for example in `git show` or when going back to it.

## Q9
The loop is: edit the files, check with `git status`, stage with `git add`, and save with `git commit` (then optionally `git log` to confirm the result). I did this twice, once for the notes and once for the README.

## Q10
README.md has a standard name and sits at the top of the repository because GitHub and other tools look for it and show it automatically on the repo's front page. It is the first thing a visitor reads, so it explains what the project is, who made it, and what it contains.

## Q11
`gh auth login` logged me in through the browser and saved an access token on my computer. It also set up Git to use that token whenever it talks to GitHub, so `git push` authenticates automatically and doesn't ask for a password.

## Q12
The front page shows the contents of my repo (files and folders) with the README.md displayed as formatted text below them. GitHub renders the README on the front page because it treats that file as the project's introduction.

## Q13
No, pushing did not change my local history. `git log --oneline` showed the same commits as before. Pushing only copies the commits to GitHub and records where the remote branch is.

## Q14
A private repository exists on GitHub, with a copy of my files and history stored there, but only I and the people I invite can see it. A repository that does not exist has no copy online at all, so there is nothing for TAs to open and no cloud backup. For outsiders both look like a "not found" page, but only the private one exists and can be shared with specific people.
