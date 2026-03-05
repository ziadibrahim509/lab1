# Lab 1 - Git & GitHub Practice

This lab contains steps to create a local repo, connect to GitHub using SSH, create commits, delete commits, and amend commits.  

## Commands Used

### 1. Initialize local repo
```bash
git init
git remote add origin git@github.com:ziadibrahim509/lab1.git
echo "<!DOCTYPE html>
<html lang='en'>
<head>
<meta charset='UTF-8'>
<title>My Lab Project</title>
</head>
<body>
<h1>Hello, my name is Ziad Ibrahim</h1>
<p>This is my lab1 HTML file for GitHub practice.</p>
</body>
</html>" > index.html
git add index.html
git commit -m "Add HTML file with my name"
git push -u origin master --force
echo "<p>Second commit content</p>" >> index.html
git commit -am "Second commit"

echo "<p>Third commit content</p>" >> index.html
git commit -am "Third commit"

echo "<p>Fourth commit content</p>" >> index.html
git commit -am "Fourth commit"
git log --oneline
git reset --hard HEAD~2
echo "<p>Commit after deletion</p>" >> index.html
git add index.html
git commit -m "commit after deletion"
echo "<p>lab Done</p>" >> index.html
git add index.html
git commit --amend -m "finish"
git push -u origin master --force

