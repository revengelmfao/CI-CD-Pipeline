# CI/CD Pipeline with GitHub Actions

![License](https://img.shields.io/badge/License-MIT-blue.svg)
<img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-blue.svg">
<img alt="Render" src="https://img.shields.io/badge/Render-Deployment-brightgreen.svg">
<img alt="Cypress" src="https://img.shields.io/badge/Cypress-Testing-orange.svg">
<img alt="MongoDB" src="https://img.shields.io/badge/MongoDB-4.4%2B-green.svg">

## Description
This repository demonstrates a CI/CD pipeline setup using GitHub Actions. The pipeline ensures code quality through automated testing and enables seamless deployment to Render when merging from `develop` to `main`.

## Table of Contents
- [Features](#features)
- [User Story](#user-story)
- [Workflow](#workflow)
- [Setup Instructions](#setup-instructions)
- [GitHub Actions Workflow](#github-actions-workflow)
- [Deployment Details](#deployment-details)
- [Resources](#resources)
- [Contribution Guidelines](#contribution-guidelines)
- [License](#license)
- [Questions](#questions)

## Features
- **Continuous Integration (CI):** Runs Cypress component tests when a Pull Request (PR) is made to the `develop` branch.
- **Continuous Deployment (CD):** Deploys the application automatically to Render when code is merged from `develop` to `main`.
- **Automated Quality Checks:** Ensures that only verified and tested code gets merged into `main`.

## User Story
```md
AS A developer integrating a CI/CD pipeline,
I WANT to run automated tests on PRs and deploy successful merges automatically,
SO THAT I can maintain code quality and streamline deployments.
```

## Workflow
1. **Feature Development:** Code changes are made in feature branches.
2. **Pull Request to `develop`:** Initiates a GitHub Action to run Cypress tests.
3. **Merge to `develop`:** Ensures tested code is integrated.
4. **Merge `develop` into `main`:** Triggers automatic deployment to Render.

## Setup Instructions
```sh
# Clone the repository
git clone https://github.com/your-username/repository-name.git

# Navigate to the project directory
cd repository-name

# Create a develop branch
git checkout -b develop

# Push the branch to GitHub
git push origin develop
```

1. Ensure GitHub Actions is enabled in your repository settings.
2. Configure Render for deployment:
   - Disable Auto-Deploy in Render settings.
   - Copy the `Deploy hook` URL for GitHub Actions.
3. Store the Render API Key in GitHub Secrets.

## GitHub Actions Workflow
Two workflows are defined:
- **CI Workflow:** Runs Cypress tests on PRs to `develop`.
- **CD Workflow:** Deploys to Render when merging `develop` into `main`.

## Deployment Details
- **Hosting Service:** Render
- **Database:** MongoDB Atlas
- **Trigger:** Merging `develop` to `main`

## Resources
- [Render Deploy Hooks](https://docs.render.com/deploy-hooks)
- [Render API Key](https://docs.render.com/api)
- [GitHub Actions Docs](https://docs.github.com/en/actions)
- [GitHub Repo Secrets](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions)

## Contribution Guidelines
- Create feature branches for changes.
- Ensure all PRs pass CI tests before merging.
- Use descriptive commit messages.

## License
This project is licensed under the MIT License.

## Questions
If you have any questions, please feel free to contact me at [bradleysantiago4@gmail.com](mailto:bradleysantiago4@gmail.com). You can also find more of my work at [https://github.com/revengelmfao](https://github.com/revengelmfao).

---
© 2024 YourName/Company. All Rights Reserved.

