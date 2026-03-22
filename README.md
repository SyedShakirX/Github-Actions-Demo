# GitHub Actions: Variables and Secrets Showcase

<div align="center">

![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![YAML](https://img.shields.io/badge/yaml-%23ffffff.svg?style=for-the-badge&logo=yaml&logoColor=151515)
![Security](https://img.shields.io/badge/Security-Secrets_Management-success.svg?style=for-the-badge)

</div>

##  Overview
This workflow serves as a technical reference and demonstration of how to properly manage data, context, and sensitive credentials within a GitHub Actions CI/CD pipeline. 

It executes two distinct jobs on a self-hosted runner to illustrate the scope and syntax of different variable types natively supported by GitHub Actions.

##  Key Concepts Demonstrated

### 1. GitHub Contexts (`${{ github.repository }}`)
Demonstrates how to dynamically access metadata about the workflow run and the repository itself without hardcoding values.

### 2. Environment Variables (`env`)
Shows how to define and utilize static variables at both the **Workflow Level** (accessible by all jobs/steps) and the **Step Level** (restricted scope).

### 3. Manual Inputs (`inputs`)
Utilizes the `workflow_dispatch` trigger to accept user-defined parameters (`num1` and `num2`) at runtime, demonstrating how to pass dynamic data into a script (e.g., performing basic arithmetic).

### 4. Secrets Management (`secrets`)
Highlights secure credential handling. It pulls a sensitive value (`${{ secrets.mysecret }}`) stored in GitHub Secrets and demonstrates how GitHub automatically masks this value (rendering as `***`) in the execution logs to prevent credential leaks.

##  How to Run
1. Navigate to the **Actions** tab in this repository.
2. Select **Workflow of Variables** from the left-hand menu.
3. Click the **Run workflow** dropdown.
4. (Optional) Override the default input numbers (`1000` and `2000`).
5. Click **Run workflow** and inspect the output logs of the `variable_job` and `secrets_job` to see how the data is handled!
 