# SQL PR Checklist

## General
- [ ] All SQL should be well-formatted, readable, and easily digested

## DDL
- [ ] DDL
  - [ ] Tables: Each entity (table) name is singular, not plural
  - [ ] Each table has a single column surrogate (primary) key constraint
  - [ ] Tables include the four standard audit columns:
      - [ ] `created_by`
      - [ ] `created_tsz`
      - [ ] `modified_by`
      - [ ] `modified_tsz`
  - [ ] Store date/time values as timestamp-TZ (Timestamps with Timezone as UTC)
  - [ ] Each table conforms to the third normal form
  - [ ] Valid value lists are kept in parent reference/lookup tables, not enums or check constraints
  - [ ] Column/Constraint/Index names conform to [Physical Model Object Naming](https://confluence.octanner.com/confluence/display/DATA/Physical+Model+Object+Naming#PhysicalModelObjectNaming-Column)
  - [ ] All DDL changes are backwards compatible

## DML
- [ ] DML
  - [ ] All DML updates/delete statements should include a WHERE clause
  - [ ] All DML updates statements should include audit columns
asdfasdfsadf