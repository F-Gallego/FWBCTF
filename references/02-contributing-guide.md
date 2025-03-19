# Contributing Guide

This repository serves as a template to help you create and maintain your own documentation or hands-on labs as code.

!!! info "Using a Template Repository"
    Instead of forking, this project uses a **GitHub Template Repository**. This allows you to create a fresh copy of the repository within your own GitHub organization.

## Contributor Workflow

Follow these steps to contribute:

1. **Create a GitHub Account** – If you don’t already have one.
2. **Use the Template Repository** – Click **"Use this template"** on [this repository](https://github.com/40docs/landing-page) to create a new repository in your GitHub organization.
3. **Request a Personal Access Token (PAT)** – Contact @ajammes or @rmordasiewicz for access.
4. **Provide Your Repository Name** – Share your new repository name with @ajammes or @rmordasiewicz.
5. **Receive Site URL** – @ajammes or @rmordasiewicz will provide a site URL for viewing your changes.
6. **Make Contributions** – Update documentation, push changes, and see updates reflected on the site URL.

??? tip "Why Use a Template Repository?"
    - Avoids issues with maintaining forks
    - Allows a fresh start while keeping upstream updates manageable
    - Enables better collaboration within an organization

## Site Structure

The navigation menu in the documentation reflects the directory structure within this repository:

!!! note "Navigation Rules"
    - **Menu item names** are derived from the `index.md` file within each sub-folder. To change the menu item name, update the top-level heading (`#`) in `index.md`.
    - **Assets and images** should be placed in a dedicated subfolder (e.g., `<subfolder>/images`).
    - **Ordering of items** can be controlled by prefixing filenames numerically (e.g., `00-intro.md`, `01-setup.md`). Menu items will be ordered alphanumerically by filename, but their displayed name comes from the top-level heading inside the file.

## Best Practices

!!! success "Follow These Guidelines"
    ✅ **Keep folder and file names concise but descriptive.**  
    ✅ **Use lowercase letters and hyphens for filenames to maintain consistency.**  
    ✅ **Organize labs sequentially or by topic for better navigation.**  

This structured approach ensures clarity, consistency, and ease of use across different teams, organizations, and labs.

---

??? question "Need Help?"
    Reach out to @ajammes or @rmordasiewicz for guidance!
