# GitHub Actions as cron jobs

This repository uses GitHub Actions to piggy-back as cron jobs to post anime GIFs 
(see https://github.com/LTLA/acceptable-anime-gifs) to various Slack channels.

1. Set up an incoming webhook for a Slack app as described [here](https://api.slack.com/messaging/webhooks).
2. Create a secret on this repository with that webhook's URL, e.g., `SLACK_WORK_WEBHOOK`.
3. Reference that secret in the workflow step that uses https://github.com/LTLA/actions-anime-gif-slackbot.

It's best to use one workflow per Slack channel for fine-grained control of the schedule.
