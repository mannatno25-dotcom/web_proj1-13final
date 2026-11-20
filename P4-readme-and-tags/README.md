# P4 - GitHub README and version tags

**Aim:** document the project with a README, mark releases with annotated tags and publish them.

**Releases:** `v0.1.0` (skeleton + About page) and `v1.0.0` (adds README). The README is in `../portfolio/README.md`.

**Publishing to GitHub:** create an empty repo on github.com, then replace the remote URL in the commands below:

```bash
git remote add origin https://github.com/<mannatno25-dotcom>/portfolio.git
git push -u origin main
git push origin --tags
```

(The transcript uses a local bare repository as the remote because GitHub cannot be reached from this environment; the commands and output format are identical.)

## Terminal output

```text

# Tag the current state as the first release
$ git tag -a v0.1.0 -m "First working skeleton with About page"
$ ls
README.md
about.html
index.html
style.css
$ git add README.md
$ git commit -m "docs: add README with structure, usage and versions"
[main 5c10dd1] docs: add README with structure, usage and versions
 1 file changed, 47 insertions(+)
 create mode 100644 README.md
$ git tag -a v1.0.0 -m "First documented release"

# List tags and inspect one
$ git tag
v0.1.0
v1.0.0
$ git tag -n
v0.1.0          First working skeleton with About page
v1.0.0          First documented release
$ git show v1.0.0 --stat
tag v1.0.0
Tagger: Your Name <you@example.com>
Date:   Wed Nov 18 04:31:05 2026 +0000

First documented release

commit 5c10dd14eccef870fec5fdd7c6ad08e0eef2aa4f
Author: Your Name <you@example.com>
Date:   Wed Nov 18 04:31:05 2026 +0000

    docs: add README with structure, usage and versions

 README.md | 47 +++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 47 insertions(+)
$ git log --oneline --decorate --graph
* 5c10dd1 (HEAD -> main, tag: v1.0.0) docs: add README with structure, usage and versions
*   6d59c27 (tag: v0.1.0) Merge feature/about-page into main
|\  
| * fdd74af feat: link about page from home navigation
| * c151f37 feat: add about page
|/  
* fd4bb94 Initial commit: add project skeleton

# Publish to a remote. For the lab use your GitHub URL; here a local bare repo stands in for GitHub so the output is real.
$ git init --bare -b main <lab>/remote.git
Initialized empty Git repository in <lab>/remote.git/
$ git remote add origin <lab>/remote.git
$ git remote -v
origin	<lab>/remote.git (fetch)
origin	<lab>/remote.git (push)
$ git push -u origin main
To <lab>/remote.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
$ git push origin --tags
To <lab>/remote.git
 * [new tag]         v0.1.0 -> v0.1.0
 * [new tag]         v1.0.0 -> v1.0.0
$ git ls-remote --tags origin
7200e0d644c5cb3d2225d746c97d46ac6c0f12a9	refs/tags/v0.1.0
6d59c27c24d95acc6d38f69cd5634fb64c779306	refs/tags/v0.1.0^{}
b2a024c11faadc7a76e8b47fb98361975e22f4a8	refs/tags/v1.0.0
5c10dd14eccef870fec5fdd7c6ad08e0eef2aa4f	refs/tags/v1.0.0^{}
```
