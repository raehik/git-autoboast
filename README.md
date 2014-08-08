git-autoboast
=============

Tweets about your last Git commit. Uses the current working directory or the
first argument as the Git repo.

Requires a 'twitterer' program to actually tweet the message. It should tweet
the first argument, and understand that URLs are automatically shortened by
Twitter (so should be smart about any length checking it does). My
`twitterminal` does the job, but just about any simple twitterer will.

The layout of a tweet is:

    "$commit_message" - commit $short_hash by $author @ $github_user/$git_root ([link to commit on GitHub])"

If the message ends up being too long, the commit message is automatically
shortened (i.e. `$commit_me...`). Not too sure how to deal with situations
where the author/GitHub user are too long as well, however.

At the moment, it tries to add a GitHub link regardless of whether the project
exists on GitHub. I'd like to fix that by adding an automatic check, plus an
switch to not include a GitHub link.
