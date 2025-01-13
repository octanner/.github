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
