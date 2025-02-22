# Contributing to Pacmax

Pacmax is a community-driven project that thrives on contributions from users like you. By updating the `repos.yml` file, you can help us feature more repositories, tools, and projects on the site. Follow the steps below to contribute.

## Why Contribute?

- **Share Your Projects:** Add your favorite repositories or projects to help the community discover great tools.
- **Keep the Site Fresh:** Ensure that Pacmax always showcases the latest and most useful contributions.
- **Support the Community:** Your input helps maintain an accurate and dynamic collection of resources for all users.

## How to Contribute

### 1. Fork the Repository

- Visit the [Pacmax GitHub repository](https://github.com/gitatmax/pacmax).
- Click the **Fork** button in the upper-right corner to create your own copy of the repository.

### 2. Clone Your Fork Locally

Run the following commands in your terminal:

```bash
git clone https://github.com/your-username/pacmax.git
cd pacmax
```

### 3. Update the repos.yml File

- Open the repos.yml file in your preferred text editor.
- Add your new repository entry following the existing YAML format, beneath `workflows:` will be the full URL of your Alfred workflow (note: we are working on adding more categories):

```yaml
- https://github.com/gitatmax/pacmax/
```

- Ensure the YAML syntax is correct (indentation matters).

### 4. Validate Your Changes

- Optionally, use a YAML linter to check for syntax errors.
- Verify that your changes follow the formatting style of the existing entries.

### 5. Commit Your Changes

Run the following commands to commit your changes locally:

```bash
git add repos.yml
git commit -m "Add new repository entry to repos.yml"
```

### 6. Create a Pull Request (PR)

Push your changes to your fork:

```bash
git push origin main
```

Then, on GitHub:

- Navigate to your forked repository.
- Click the Compare & pull request button.
- Provide a clear description of your contribution.
- Submit the pull request for review.

### 7. Review Process

- our PR will be reviewed by the Pacmax maintainers.
- If any changes are requested, update your PR accordingly.
- Once approved, your contribution will be merged, and your repository will be featured on Pacmax.

## Need Help?

If you have any questions or need further assistance:

- Open an issue on the Pacmax GitHub issues page.
- Contact one of the maintainers for guidance.

Happy contributing!
