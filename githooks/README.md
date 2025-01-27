# Git Hooks for Sorting Algorithm Visualizer

This repository contains a collection of Git hooks designed to enforce a clean commit policy for your **Sorting Algorithm Visualizer** project.

## Git Hooks Overview
1. **`pre-commit`**: Prevents direct commits to the `master` branch to ensure better code management.
2. **`commit-msg`**: Ensures commit messages follow consistent and predefined formatting rules.
3. **`.git-commit-msg-template.txt`**: Provides a commit message template to help developers follow the conventions.

---

## Installation

### Step 1: Clone the Repository
Clone the repository to your local machine:

```bash
git clone https://github.com/YourUsername/Sorting-Algorithm-Visualizer.git
cd Sorting-Algorithm-Visualizer
```

---

### Step 2: Set Up Commit Message Template
To standardize commit messages, you can set up a template:

1. Copy the provided `.git-commit-msg-template.txt` file to a preferred location (e.g., your home directory):

   ```bash
   cp .git-commit-msg-template.txt ~/.git-commit-msg-template
   ```

2. Configure Git to use the commit message template globally:

   ```bash
   git config --global commit.template ~/.git-commit-msg-template
   ```

Now, every time you commit changes, the template will guide you to write clear and consistent commit messages.

*Tip:* If you're using a Git client like PhpStorm, consider integrating the template directly for seamless use.

---

### Step 3: Install Git Hooks

You can install the hooks for either a **single repository** or **globally** for all repositories.

#### Single Repository Installation
To apply the hooks only to this repository:

1. Copy the `pre-commit` and `commit-msg` hook files to the repository's `.git/hooks` directory:

   ```bash
   cp pre-commit commit-msg .git/hooks/
   chmod +x .git/hooks/pre-commit .git/hooks/commit-msg
   ```

#### Global Installation
To apply the hooks across all repositories:

1. Create a global Git hooks directory:

   ```bash
   mkdir -p ~/.git-template/hooks
   ```

2. Configure Git to use this directory as the global template:

   ```bash
   git config --global init.templatedir '~/.git-template'
   ```

3. Copy the hook files to the global hooks directory:

   ```bash
   cp pre-commit commit-msg ~/.git-template/hooks
   chmod +x ~/.git-template/hooks/pre-commit ~/.git-template/hooks/commit-msg
   ```

4. For existing repositories, reinitialize Git to apply the hooks:

   ```bash
   git init
   ```

---

## Configuration

You can customize the behavior of the Git hooks using Git configuration commands.

### Append Branch Name to Commit Messages
To automatically append the current branch name to commit messages:

```bash
git config git-hooks.append-branch-name true
```

To disable this behavior:

```bash
git config git-hooks.append-branch-name false
```

---

### Enable Committing on the `master` Branch
By default, committing directly to the `master` branch is disabled. To allow commits on `master`:

```bash
git config git-hooks.commit-on-master true
```

To disable committing on `master` again:

```bash
git config git-hooks.commit-on-master false
```

---

### Global Configuration
To apply these settings globally, add the `--global` flag:

```bash
git config --global git-hooks.append-branch-name true
git config --global git-hooks.commit-on-master true
```

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch:  
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes following the commit message guidelines.
4. Push to your branch:  
   ```bash
   git push origin feature/your-feature
   ```
5. Open a pull request.

---

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

