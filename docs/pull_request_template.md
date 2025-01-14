
We are excited to announce that we have centralized our common PR checklist items across all repositories in the organization. 
These checklists are now available in our organization-wide GitHub templates. We have `SQL PR Checklist` for now, and we will be adding more in the future. 

> Feel free to make any suggestions or improvements to these templates. PR is always welcome!

You can find the templates here: [org wide GitHub templates](https://github.com/octanner/.github/blob/main/docs/)

This effort aims to streamline the PR review process and ensure consistency across all projects. If needed, you can override these checklists by creating a new file in your own repository.  
For more information, please refer to: [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file).  

Thank you for your cooperation and happy coding!
<hr></hr> 

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
