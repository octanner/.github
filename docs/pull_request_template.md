# SQL PR Checklist

## General
- [ ] All SQL should be well-formatted, readable, and easily digested

## DDL
- [ ] Database/Schmea
    - [ ] Conforms to the Third Normal Form
    - [ ] Valid value lists are kept in parent reference/lookup tables, not enums or check constraints
    - [ ] All changes are backwards compatible
- [ ] Tables
  - [ ] Entity names are singular, not plural
    - [ ] Has a single column surrogate (primary) key constraint
    - [ ] Includes the four standard audit columns:
        - [ ] `created_by` as timestamptz
        - [ ] `created_tsz` as timestamptz
        - [ ] `modified_by` as timestamptz
        - [ ] `modified_tsz` as timestamptz
    - [ ] Has indexes on foreign keys
    - [ ] Has indexes indexes on `created_tz` and `modified_tz` columns
- [ ] Columns
    - [ ] Store date/time values as timestamp-TZ (Timestamps with Timezone as UTC)
    - [ ] Constraint/Index names conform to [Physical Model Object Naming](https://confluence.octanner.com/confluence/display/DATA/Physical+Model+Object+Naming#PhysicalModelObjectNaming-Column)

## DML
- [ ] All DML updates/delete statements should include a WHERE clause
- [ ] All DML updates statements should include audit columns

# Java PR Checklist

Note: this is for testing purposes only. We have to come up with a better checklist for Java PRs.

- [ ] The code compiles without errors.
- [ ] All tests pass.
- [ ] Code is properly formatted.
- [ ] No new warnings are introduced.
- [ ] Documentation is updated if necessary.
- [ ] Changes are backward-compatible.
- [ ] Code follows the project's coding standards.
- [ ] Commit messages are clear and descriptive.
