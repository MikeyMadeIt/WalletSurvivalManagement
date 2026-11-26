
# Contributing Guidelines

Thank you for contributing to the **Wallet Survival Management System**!

This document outlines the development workflow, coding standards, and collaboration guidelines for all team members.

## 1. Project Overview

The Wallet Survival Management System is a VB.NET console application built with .NET 10 and SQLite. It focuses on personal financial management, including income, expenses, budgets, savings, transaction records, and financial survival analysis.

## 2. Repository Structure

The repository follows a modular project structure.

- `WalletSurvivalManagement/` - Main VB.NET application.
- `Models/` - Data models and entity representations.
- `Data/` - Database connection and initialization.
- `Repositories/` - Database queries and data persistence.
- `Services/` - Business logic and system operations.
- `DataStructures/` - Data structure implementations.
- `Algorithms/` - Searching, sorting, and calculation algorithms.
- `Menus/` - Console menus and user interaction.
- `Database/` - Database-related files.
- `docs/` - Project documentation, pseudocode, flowcharts, and database design.

## 3. Branching Strategy

The project uses a branch-based workflow to organize development.

### Main Branches

| Branch | Purpose |
|---|---|
| `main` | Stable and approved project version. |

### Member Branches

Each member has an assigned development branch.

| Member | Branch |
|---|---|
| Mikey | `dev/mikey` |
| Mapalo | `dev/mapalo` |
| Lopez | `dev/lopez` |
| Tejada | `dev/tejada` |
| Felix | `dev/felix` |

### Branch Rules

1. Do not directly push feature changes to `main`.
2. Work on your assigned development branch.
3. Keep your branch updated with the integration branch when applicable.
4. Submit a Pull Request when your changes are ready.
5. Resolve merge conflicts before completing a merge.
6. Do not merge untested or incomplete changes into `main`.

## 4. Development Workflow

Follow these steps when contributing:

### Step 1: Switch to Your Assigned Branch

```bash
git switch dev/your-name
git pull origin dev/your-name
```

### Step 2: Make Your Changes

- Work only on your assigned modules or approved tasks.
- Follow the existing folder structure.
- Avoid modifying files assigned to other members without coordination.
- Keep changes focused on one feature or task.

### Step 3: Test Your Changes

Before committing, build the project:

```bash
dotnet build
```

Run the application when applicable:

```bash
dotnet run
```

### Step 4: Commit Your Changes

Use clear and descriptive commit messages.

```bash
git add .
git commit -m "feat: add income management"
git push origin dev/your-name
```

### Step 5: Create a Pull Request

- Open the repository on GitHub.
- Create a Pull Request from your development branch.
- Set the base branch to `develop`.
- Provide a clear description of your changes.
- Request a review from the project integrator or assigned reviewer.

## 5. Commit Message Convention

Use the following prefixes:

| Prefix | Usage |
|---|---|
| `feat:` | Adding a new feature. |
| `fix:` | Fixing a bug or error. |
| `docs:` | Updating documentation. |
| `refactor:` | Improving existing code without changing behavior. |
| `style:` | Formatting and code style changes. |
| `test:` | Adding or modifying tests. |
| `chore:` | Project configuration and maintenance. |

Examples:

```text
feat: add expense management
fix: correct wallet balance calculation
docs: update database documentation
refactor: improve transaction service
test: add budget calculation tests
chore: update project structure
```

## 6. Coding Standards

All contributors must follow these guidelines:

- Use VB.NET for application development.
- Follow consistent naming conventions.
- Use PascalCase for class names, methods, and properties.
- Use meaningful and descriptive variable names.
- Keep methods focused on a single responsibility.
- Avoid unnecessary code duplication.
- Add comments when logic needs clarification.
- Validate user input before processing.
- Handle exceptions appropriately.
- Use parameterized SQL queries when accessing SQLite.
- Store monetary values in integer centavos in the database to avoid floating-point precision issues.

## 7. Data Structures and Algorithms

Data structures and algorithms are important parts of this project.

Planned data structures:

- `List(Of T)` - Managing collections of transactions.
- `Dictionary(Of TKey, TValue)` - Grouping expense totals by category.
- `Stack(Of T)` - Managing recent operations for undo functionality.

Planned algorithms:

- Linear Search - Finding specific transactions.
- Bubble Sort - Sorting transaction records.
- Expense Grouping - Organizing expenses by category.
- Budget Calculation - Computing budget usage and remaining amounts.
- Survival Calculation - Estimating how long the remaining balance can last.

Implementations must be functional and integrated into the application.

## 8. Documentation Guidelines

Update the documentation whenever a relevant system feature or design changes.

Documentation is maintained in the `docs/` directory.

- `pseudocode/` - Logical steps of system operations.
- `flowcharts/` - Visual representations of system processes.
- `database/` - Database schema and relationship documentation.
- `team/` - Team assignments and collaboration guidelines.

Keep documentation consistent with the actual implementation.

## 9. Pull Request Guidelines

Before submitting a Pull Request:

- Ensure the project builds successfully.
- Test the affected functionality.
- Check that no unrelated files are included.
- Write a descriptive Pull Request title.
- Explain what changed and why.
- Mention any known issues or incomplete work.

Pull Requests should be reviewed before merging into `develop`.

Only tested and approved changes from `develop` should be merged into `main`.

## 10. General Team Guidelines

1. Communicate with the team before making major structural changes.
2. Respect assigned responsibilities.
3. Avoid overwriting another member's work.
4. Keep your branch updated.
5. Report blockers and technical issues early.
6. Prioritize readable, maintainable, and functional code.
7. Keep the repository organized.

---

**Note:** These guidelines may be updated as the project develops and the team agrees on improvements.

**Project:** Wallet Survival Management System  
**Language:** VB.NET  
**Framework:** .NET 10  
**Application Type:** Console Application  
**Database:** SQLite
