
## Initializing a New Module or Project

### Using the Default `npm init` Command

```bash
npm init
```

### Using `npm init -y` or `npm init --yes`

```bash
npm init -y
```

```bash
npm init --yes
```

### **Using `npm init --scope=@scope-name`**

For initializing a project under a specific scope (for scoped packages).
Scoped packages are namespaced and are often used for private or organizational modules.

```bash
npm init --scope=@myscope
```

### Using Custom `npm init` Templates

```bash
npm init react-app
```

## Installing Dependencies

### Installing Regular Dependencies

```bash
npm install <package-name>
```

Eg. specific version of Express

```bash
npm install express@4.18.2
```

### Installing Development Dependencies

```bash
npm install <package-name> --save-dev
```

or 
```bash
npm install <package-name> -D
```

### Installing Global Packages

```bash
npm install -g <package-name>
```

### Installing Peer Dependencies

Some packages require specific peer dependencies. While npm doesn’t install these automatically, you can install them manually:

```bash
npm install <peer-dependency-name>
```

### Installing Optional Dependencies

```bash
npm install <package-name> --save-optional
```

### Installing from a Git Repository

```bash
npm install git+https://github.com/user/repo.git
```

### Installing from a Local Folder

```bash
npm install /path/to/local/folder
```

### Installing with `package-lock.json`

If you have a `package-lock.json` file and you want to install dependencies exactly as they are specified in the lock file, just run:

```bash
npm ci
```

### Installing Multiple Packages at Once

```bash
npm install <package-1> <package-2> <package-3>
```

### Rebuilding Native Dependencies

```bash
npm rebuild
```

## Auditting the `package.json` File

### Running an Audit

```bash
npm audit
```

### Fixing Vulnerabilities Automatically

```bash
npm audit fix
```

### Fixing All Issues, Including Breaking Changes

Be cautious with this command, as it can update major versions and potentially break your project.

```bash
npm audit fix --force
```

### Detailed Vulnerability Report

This will return a JSON-formatted report, which might be useful for integration with CI/CD pipelines or logging tools.

```bash
npm audit --json
```

### Auditing Specific Dependency Levels

Available levels are:

- `low`
- `moderate`
- `high`
- `critical`

```bash
npm audit --audit-level=critical
```

### Ignoring Specific Issues

Sometimes there are vulnerabilities that you want to ignore (e.g., because they are false positives or they don't apply to your project). You can generate an "ignore report" by running:

However, this isn't a long-term solution, and you should try to handle the vulnerabilities properly.

```bash
npm audit fix --ignore
```

### Manually Fixing Vulnerabilities

If `npm audit fix` doesn't resolve an issue, you may need to manually update specific packages. You can do this by checking the vulnerability report and updating the vulnerable package directly:

```bash
npm install <package-name>@latest
```

### Auditing in CI/CD Pipelines

This will generate a report that can be integrated into automated build processes, ensuring that no insecure dependencies make it into production.

```bash
npm audit --json > audit-report.json
```

## Updating All Packages

```bash
npm update
```

## Removing Dependency

```bash
npm uninstall <package>
```

