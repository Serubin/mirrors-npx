npx mirror
================

Mirror of npx package for pre-commit.

For pre-commit: see https://github.com/pre-commit/pre-commit

For npx: see https://github.com/zkat/npx


### Using npx with pre-commit

Add this to your `.pre-commit-config.yaml`:

    -   repo: https://github.com/pre-commit/mirrors-npx
        rev: ''  # Use the sha / tag you want to point at
        hooks:
        -   id: npx

When using plugins with `npx` you'll need to declare them under
`additional_dependencies`. For example:

    -   repo: https://github.com/pre-commit/mirrors-npx
        rev: ''  # Use the sha / tag you want to point at
        hooks:
        -   id: npx
            additional_dependencies:
            -   npx@4.15.0
            -   eslint@6.10.3
