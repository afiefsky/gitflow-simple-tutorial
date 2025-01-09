# Simple GitFlow Tutorial

GitFlow is a branching model for Git, designed to help teams collaborate effectively on software development projects. Follow these steps to get started:

---

## 1. Setup GitFlow

If you’re using GitFlow for the first time in a repository, install it with:

```bash
git flow init
```

You'll be prompted to set up branch names. By default:
- **Main branch:** `main` (or `master`)
- **Development branch:** `develop`

You can press `Enter` to accept the defaults.

---

## 2. The Main Branches

- **Main (`main`)**: Contains production-ready code.
- **Develop (`develop`)**: Contains code for the next release, built by merging feature branches.

---

## 3. Feature Branches

Feature branches are for developing new features.

### Create a feature branch:
```bash
git flow feature start feature-name
```

### Work on the feature:
- Make changes.
- Commit the changes:
  ```bash
  git add .
  git commit -m "Your commit message"
  ```

### Finish the feature:
```bash
git flow feature finish feature-name
```

This merges the feature branch into `develop` and deletes the feature branch.

---

## 4. Release Branches

Release branches are used to prepare for a new production release.

### Create a release branch:
```bash
git flow release start release-version
```

### Work on the release:
- Make any final changes.
- Commit them.

### Finish the release:
```bash
git flow release finish release-version
```

This merges the release branch into both `main` and `develop`, creates a version tag, and deletes the release branch.

---

## 5. Hotfix Branches

Hotfix branches are for fixing critical issues in production.

### Create a hotfix branch:
```bash
git flow hotfix start hotfix-name
```

### Work on the hotfix:
- Make changes.
- Commit the changes.

### Finish the hotfix:
```bash
git flow hotfix finish hotfix-name
```

This merges the hotfix branch into both `main` and `develop`, creates a version tag, and deletes the hotfix branch.

---

## 6. Commands Summary

| Action        | Command                               |
|---------------|---------------------------------------|
| Initialize GitFlow | `git flow init`                 |
| Start feature  | `git flow feature start feature-name` |
| Finish feature | `git flow feature finish feature-name` |
| Start release  | `git flow release start release-version` |
| Finish release | `git flow release finish release-version` |
| Start hotfix   | `git flow hotfix start hotfix-name`   |
| Finish hotfix  | `git flow hotfix finish hotfix-name`  |

---

## 7. Best Practices

- Keep feature branches small and focused.
- Regularly pull changes from `develop` into your feature branch to stay updated.
- Use meaningful branch names.

GitFlow helps maintain clean and organized workflows, ensuring smooth collaboration and deployment.
