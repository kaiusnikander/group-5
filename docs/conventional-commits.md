# Conventional Git commits

You are **required** to follow this concept of `conventional commits`. Following this guide will ensure your commits are concise and readable. Which in turn makes sure that the commit history for the whole project is clear, manageable and easy to understand.

A single commit should contain a specific, well-defined change.

In case this document is confusing, or you would like more information about `conventional commits` there are some [references](#references) below.

`VSCode` has an extension named `Conventional Commits` which can make this whole process more streamlined. If you are interested in taking this extension into use, you can find our guide [here](../extensions/conventional-commits.md)

## Default

This depicts how the commit message should look when typing in the commit message manually. By clicking on the links you will be taken to a section that will tell you more about that specific part of the message.

<pre>
<b><a href="#types">type</a></b></font>(<b><a href="#scopes">optional scope</a></b>): <b><a href="#description">description</a></b>
<sub>empty separator line</sub>
<b><a href="#body">optional body</a></b>
<sub>empty separator line</sub>
<b><a href="#footer">optional footer</a></b>
</pre>

Commit message examples can be found at the bottom of this document or by following [this link](#examples)

## Commit types

- Changes related to API
  - `feat`: You have added or removed a new feature
  - `fix`: You have fixed a bug
- Changes related to code cleanness
  - `refactor`: You have rewritten or restructured your code, but API behavior has not changed
    - `perf`: This is a special `refactor` commit which improves performance
  - `style`: You have changed the code functions. (White-space changes, formatting, missing semi-colons, etc)
- Other types of commits
  - `docs`: You have added new documentation or changed old
  - `test`: You have added missing tests or corrected existing ones
  - `build`: You commit affects build components, like build tool, dependencies, project version, etc
  - `ops`: Your commit affects operational components, like infrastructure, backup, recovery, etc
  - `chore`, `misc`: Miscellaneous commits, like modifying `.gitignore`

## Scopes

The `scope` identifier provides additional information.

- This is an **optional** part of the format, but highly recommended
- Only use routes as an identifier, like `application`, `profile`

## Breaking changes indicator

Breaking changes should be indicated by an `!` before the `:` in the subject line e.g. `feat(api)!: remove status endpoint`

- Is an **optional** part of the format

## Description

`description` contains a concise description of the change.

- This is **MANDATORY**
- Use "change", not "changed" or changes"
  - Think `This commit will...` or `This commit should`
  - Do **not** write this part in the commit though
- Don't capitalize the first letter
- There should be no (`.`) at the end

## Body

`body` should include why this change was made

- This is **optional**
- Use change instead of "changed" or "changes"

## Footer

`footer` should contain information about **Breaking Changes**

- This is **optional**
- **Breaking Changes** should start with the word `BREAKING CHANGES:` followed by space or two newlines. The rest of the message is then used for explaining the changes

## References

This is easier to read:  
<https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13#scopes>

This site contains more information about conventional commits:  
<https://www.conventionalcommits.org/en/v1.0.0/>

## Examples

---

    feat: add email notifications on new direct messages

---

    feat(profile): add the amazing button

---

    feat!: remove ticket list endpoint

---

    BREAKING CHANGES: ticket endpoints no longer supports list all entities.

---

    fix(api): handle empty message in request body

---

    fix(api): fix wrong calculation of request body checksum

---

    fix: add missing parameter to service call

    The error occurred because of <reasons>.

---

    perf: decrease memory footprint for determine unique visitors by using HyperLogLog

---

    build: update dependencies

---

    build(release): bump version to 1.0.0

---

    refactor: implement fibonacci number calculation as recursion

---

    style: remove empty line
