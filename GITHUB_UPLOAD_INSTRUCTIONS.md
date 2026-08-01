# Uploading this project to GitHub

## Browser method

1. Sign in to GitHub.
2. Select **New repository**.
3. Enter a repository name such as `robust-linear-regression-outliers`.
4. Add a short description.
5. Choose **Public** if the notebook should accompany the TDS article.
6. Do not initialize the repository with a README because this package
   already contains one.
7. Create the repository.
8. Select **uploading an existing file**.
9. Drag all files and the `figures` folder from this package into the
   upload area.
10. Enter a commit message such as `Initial publication-ready release`.
11. Select **Commit changes**.

## Git command-line method

From inside this project folder:

```bash
git init
git add .
git commit -m "Initial publication-ready release"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/robust-linear-regression-outliers.git
git push -u origin main
```

Replace `YOUR-USERNAME` with the GitHub account name.

## Before sharing the repository

- Confirm that the notebook renders correctly on GitHub.
- Add the final TDS article link to `README.md` after publication.
- Select a repository license if reuse is intended.
- Verify that no private paths, credentials, tokens, or personal data are
  present.
