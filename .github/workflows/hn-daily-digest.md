---
on:
  workflow_dispatch:
permissions:
      contents: read
      issues: read
      pull-requests: read
engine: copilot
network:
  allowed:
    - hacker-news.firebaseio.com
tools:
  github:
    toolsets: [default]
  web-fetch:
safe-outputs:
  create-issue:
---

# hn-daily-digest

Skip all design, planning, and documentation steps. Directly execute the following task immediately:

Create a daily digest workflow for professional developers, referencing relevant top Hacker News stories on technology that can be used today by large companies. Every weekday, fetch the top 30 stories from the Hacker News API (https://hacker-news.firebaseio.com/v0/topstories.json), filter to stories with a score above 50 that are about software engineering, cloud infrastructure, AI/ML, developer tooling, or distributed systems. For each qualifying story include: the title, the URL, the score, the number of comments, and a one-sentence summary of why it is relevant to enterprise developers. Create a GitHub issue titled "HN Digest - <date>" with the results formatted as a Markdown table.

<!--
## TODO: Customize this workflow

The workflow has been generated based on your selections. Consider adding:

- [ ] More specific instructions for the AI
- [ ] Error handling requirements
- [ ] Output format specifications
- [ ] Integration with other workflows
- [ ] Testing and validation steps

## Configuration Summary

- **Trigger**: Manual trigger
- **AI Engine**: copilot
- **Tools**: github, web-fetch, web-search
- **Safe Outputs**: create-issue
- **Network Access**: defaults

## Next Steps

1. Review and customize the workflow content above
2. Remove TODO sections when ready
3. Run `gh aw compile` to generate the GitHub Actions workflow
4. Test the workflow with a manual trigger or appropriate event
-->
