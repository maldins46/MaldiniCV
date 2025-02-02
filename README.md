# MaldiniCV

This repository contains my CV written in LaTeX. A GitHub Action is set up to automatically generate a PDF and create a release whenever a new tag is pushed to the `main` branch.

## 📜 Features

- Written in **LaTeX** for high-quality typesetting.
- **GitHub Actions** automates PDF generation.
- Automatically **creates a GitHub release** with the generated PDF.
- Follows **Semantic Versioning** for release tagging.

## 📂 Repository Structure

```
/
├── .github/workflows/build-and-release.yml  # GitHub Action workflow
├── src                                      # LaTeX source files for CV
├── README.md                                # Project documentation
```

## 🚀 Usage

### 1. Clone the repository

```sh
git clonehttps://github.com/maldins46/MaldiniCV.git
cd your-cv-repo-folder
```

### 2. Edit `main.tex`

Modify the LaTeX file to update your CV content.

### 3. Commit and push changes

```sh
git add cv-maldini.tex
git commit -m "Update CV"
git push origin main
```

### 4. Create a new release

Push a new tag following **Semantic Versioning** (e.g., `v1.0.0`):

```sh
git tag v1.0.0
git push origin v1.0.0
```

This triggers the GitHub Action, which:

1. **Compiles `cv-maldini.tex`** into `cv-maldini.pdf`
2. **Uploads `cv-maldini.pdf`** as a release asset

### 5. Download the PDF

Go to the **Releases** section on GitHub to download the latest version.

## 🛠️ Dependencies

The workflow installs the following LaTeX packages:

- `texlive-latex-base`
- `texlive-latex-extra`
- `texlive-fonts-recommended`
- `texlive-lang-european`

## 📄 License

This project is licensed under the MIT License.

## 📧 Contact

For any questions or improvements, feel free to open an issue or submit a pull request!
