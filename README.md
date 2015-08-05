# Ansible Playground
##### An examination of interesting features of the provisioning tool

Unless otherwise stated, results here have been found with Ansible version 1.9.2.

This repository is broken up into a number of examinations. Each examination will be listed below with a link to the associated git branch on which the examination was performed.

## Examinations

### [examination/dependency_repetition]()

I set one role, `_dep`, as a dependency of each of two other roles, `foo` and `bar`, and then tried modifying how the role was a dependent, noting how the dependency was called in each situation.

**Results:**
- When two roles depend on the same role with no modifiers, the dependency is called exactly once.
- When two roles depend on the same role with the same tag, the dependency is called exactly once.
- When two roles depend on the same role with different tags, the dependency is called prior to each dependent role.


[examination/dependency_repetition]: https://github.com/schlueter/ansible-playground/tree/examination/dependency_repetition
