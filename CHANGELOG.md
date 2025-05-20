# Changelog

## 2025-05-19
- **Fixed**: Incorrect Git repository structure by removing .git from fusion-news-agent and re-cloning hyperpoint.github.io.
- **Updated**: Reprocessed all existing articles to include updated tone (specific examples, global context), authorship disclosure, and authority signals.

## 2025-05-20
- **Fixed**: Updated sync_repo.sh to avoid adding untracked files and use GITHUB_TOKEN.
- **Updated**: Reprocessed articles with latest changes.

## 2025-05-20 (continued)
- **Added**: Immediate publishing option with --immediate flag in fusion_news_agent.py while preserving scheduling for production.
