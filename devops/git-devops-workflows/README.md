# Git DevOps Workflow Simulation

This project demonstrates a hands-on Git workflow simulating real-world DevOps practices, including branching, committing changes, merging, and pushing to a remote repository.

---

## 📌 Scenario

A development team is working on a shared repository. New features are developed in isolated branches, tested, and then merged back into the main branch (`master`). Changes are then pushed to a remote repository.

---

## ⚙️ Workflow Steps

### 1. Create and Switch to Feature Branch
```
git checkout -b nautilus-t2q3
```

### 2. Add New File to Repository

```
cp /tmp/index-t2q3.html
```

### 3. Stage and Commit Changes
```
git add index-t2q3.html
git commit -m "Added index file"
```

### 4. Switch Back to Master Branch
```
git switch master
```

### 5. Merge Feature Branch into Master
```
git merge nautilus-t2q3
```

### 6. Push Changes to Remote Repository
```
git push origin master
git push origin nautilus-t2q3
```

## 🧠 Key Concepts Demonstrated
Branching strategy (feature branches)
Staging and committing changes
Merging branches
Working with remote repositories (origin)
Understanding Git workflow in a DevOps context

## ⚠️ Challenges & Lessons Learned
Branches are not directories — switching branches does not change folders
Correct push syntax matters:

```
git push <remote> <branch>
```

# Order of operations is critical:
- Create branch → Add changes → Commit → Merge → Push
# Understanding errors leads to faster troubleshooting

## 🚀 Real-World Relevance

This workflow mirrors how:
-Infrastructure changes (Terraform, Kubernetes YAML, etc.) are managed
-Teams collaborate using feature branches
-CI/CD pipelines are triggered from Git events

## 🛠️ Tools Used
-Git (CLI)
-Linux environment (file operations)
