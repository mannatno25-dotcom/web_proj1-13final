# P3 - Feature-branch Git workflow

**Aim:** develop a feature on its own branch, then merge it into `main`.

**Workflow:** `git switch -c feature/about-page` -> two commits -> `git switch main` -> `git merge --no-ff` -> `git branch -d`.

**Why `--no-ff`:** it always creates a merge commit, so the history graph shows that a feature branch existed.

## Terminal output

```text

# Create and switch to a feature branch
$ git switch -c feature/about-page
Switched to a new branch 'feature/about-page'
$ git branch
* feature/about-page
  main

# Commit 1 on the feature branch
$ git add about.html
$ git commit -m "feat: add about page"
[feature/about-page c151f37] feat: add about page
 1 file changed, 21 insertions(+)
 create mode 100644 about.html

# Commit 2: link the new page from the home page
$ sed -i 's#<a href="index.html">Home</a>#<a href="index.html">Home</a>\n      <a href="about.html">About</a>#' index.html
$ git diff
diff --git a/index.html b/index.html
index 0aac02d..6938d4d 100644
--- a/index.html
+++ b/index.html
@@ -11,6 +11,7 @@
     <h1>My Portfolio</h1>
     <nav>
       <a href="index.html">Home</a>
+      <a href="about.html">About</a>
     </nav>
   </header>
   <main>
$ git commit -am "feat: link about page from home navigation"
[feature/about-page fdd74af] feat: link about page from home navigation
 1 file changed, 1 insertion(+)
$ git log --oneline --graph --all
* fdd74af feat: link about page from home navigation
* c151f37 feat: add about page
* fd4bb94 Initial commit: add project skeleton

# Switch back to main (about.html is not here yet) and merge with a merge commit
$ git switch main
Switched to branch 'main'
$ ls
index.html
style.css
$ git merge --no-ff feature/about-page -m "Merge feature/about-page into main"
Merge made by the 'ort' strategy.
 about.html | 21 +++++++++++++++++++++
 index.html |  1 +
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
$ ls
about.html
index.html
style.css

# Clean up the finished branch and view history
$ git branch -d feature/about-page
Deleted branch feature/about-page (was fdd74af).
$ git log --oneline --graph --all
*   6d59c27 Merge feature/about-page into main
|\  
| * fdd74af feat: link about page from home navigation
| * c151f37 feat: add about page
|/  
* fd4bb94 Initial commit: add project skeleton
```
