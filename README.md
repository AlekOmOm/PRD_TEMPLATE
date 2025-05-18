# PRD_TEMPLATE

A structured framework for creating component-based Product Requirements Documents that facilitate clear development tracking and task assignment.

## Purpose

This repository provides templates for creating modular Product Requirements Documents (PRDs) that:

1. Break down complex products into discrete, manageable components
2. Enable parallel development workflows
3. Create explicit connections between specifications and implementation tasks
4. Maintain a single source of truth while distributing development focus

## Repository Structure

```
PRD_TEMPLATE/
├── PRD.md              # Main PRD document with high-level specifications
├── components/         # Individual component specifications
│   ├── COMPONENT.md    # Template for component documentation
│   └── ...             # Actual component specifications
├── TASKS.md            # Optional: Task tracking with component references
└── README.md           # This guide
```

## Usage Guidelines

### Getting Started

1. Clone this repository to create a new PRD
2. Complete the main `PRD.md` with your product's overview information
3. Identify logical components of your system
4. Create component files in the `components/` directory using the `COMPONENT.md` template
5. Reference components in the main PRD using the linking convention
6. Link tasks to specific component requirements

### Component Identification

Components should represent discrete, cohesive parts of your system that:

- Serve a specific function
- Have clear boundaries and interfaces
- Can be developed relatively independently
- Have a manageable scope (neither too broad nor too granular)

Examples: Authentication System, Data Storage, User Interface, API Layer

### Reference System

Use GitHub's native cross-file reference system:

- From PRD to component: `See [Authentication Component](./components/authentication.md)`
- From task to requirement: `Implements [Authentication: Password Reset](../components/authentication.md#password-reset)`
- From component to component: `Depends on [Data Storage](./data-storage.md#user-schema)`

### Versioning Components

When components evolve:

1. Document changes clearly in the component file
2. Use GitHub's history tracking to maintain version control
3. Consider adding a version number in the component header
4. Link issues and pull requests to specific component changes

## Best Practices

1. **Component Granularity**: Keep components focused enough to be comprehensible but broad enough to be meaningful
2. **Explicit Dependencies**: Clearly document how components interact with each other
3. **Consistent Formatting**: Follow the templates strictly for readability
4. **Complete Documentation**: Never leave template sections empty - if not applicable, state why
5. **Maintain References**: Keep cross-references updated when components change
6. **Task Linking**: Always connect implementation tasks to specific component requirements

## Template Usage Rules

1. Do not modify the structure of template files
2. Complete all sections of the templates
3. Use consistent naming conventions for all files
4. Maintain relative links between documents
5. Follow Markdown formatting for readability

## Contributing

When contributing to this template system:

1. Suggest improvements via issues
2. Maintain backward compatibility with existing PRDs
3. Document template changes thoroughly
4. Test templates with real product examples

## License

MIT License
