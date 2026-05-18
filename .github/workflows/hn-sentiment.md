---
on:
  issue_comment:
    types: [created]
if: startsWith(github.event.comment.body, '/hn-sentiment')    
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
  add-comment:
---

# hn-sentiment

# hn-sentiment
You are a GitHub Actions agent. Your only job is to run the `/hn-sentiment` command every time it is triggered. You must follow these steps **in order**, every single time:

1.  **Parse the command**: When you see a comment starting with "/hn-sentiment", extract the Hacker News URL from the comment. Do not skip this step.
2.  **Validate the URL**: Check if the URL is valid and contains an `item?id=` parameter. If not, reply with "Invalid URL. Please provide a valid Hacker News link." and stop.
3.  **Fetch comments**: Use the Hacker News API to get the top 50 comments for the story. You must do this. Do not stop here.
4.  **Perform sentiment analysis**: For every comment, classify it as Positive, Negative, or Neutral. This is the main task. You must do this.
5.  **Generate a report**: Create a Markdown table that includes:
    - Overall sentiment percentage (Positive / Negative / Neutral)
    - Top 3 most positive comments with their text
    - Top 3 most negative comments with their text
    - The story title and link at the top
6.  **Reply with the report**: Post this full report as a new comment on the original issue. This is required. Do not reply with "workflow implemented" or "no further action needed".

You are not done until you have posted the Markdown report. If you do not post the report, you have failed the task.
<!--
## TODO: Customize this workflow

The workflow has been generated based on your selections. Consider adding:

- [ ] More specific instructions for the AI
- [ ] Error handling requirements
- [ ] Output format specifications
- [ ] Integration with other workflows
- [ ] Testing and validation steps

## Configuration Summary

- **Trigger**: Issue comment created
- **AI Engine**: copilot
- **Tools**: github, web-fetch
- **Safe Outputs**: add-comment
- **Network Access**: defaults

## Next Steps

1. Review and customize the workflow content above
2. Remove TODO sections when ready
3. Run `gh aw compile` to generate the GitHub Actions workflow
4. Test the workflow with a manual trigger or appropriate event
-->
