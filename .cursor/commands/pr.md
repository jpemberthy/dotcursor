# Open Pull Request

Automatically create a pull request by:
1. Examining the current branch diff against main to understand all changes
2. Generating a comprehensive PR description using the project's PR template format
3. Adding all changes, committing, pushing, and creating a draft PR

Execute the full automated workflow: `git add . && git commit -m "Generated commit message based on changes" && git push origin $(git branch --show-current) && gh pr create --draft --title "Generated PR title" --body "Generated PR description using .github/pull_request_template.md format"`

The PR description will be generated in RAW markdown format following the `.github/pull_request_template.md` structure with:
- Summary section with Linear issue links and related PRs (pre-fill Linear Issue with "Part of <current-branch-name>")
- Description of changes and accomplishments
- Tests checklist (unit and integration tests)
- Considerations for edge cases and deployment impacts

All file changes from the branch diff will be captured to ensure complete context in the PR description.

