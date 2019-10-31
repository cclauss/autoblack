# autoblack
### GitHub Action that uses Black to reformat Python code in incoming pull requests.
If all Python code in the pull request is complient with Black then this Action does nothing.

Othewrwise, Black is run and a new commit with reformatted code is added to the incoming pull request.

Inspired by:
https://peterevans.dev/posts/github-actions-how-to-automate-code-formatting-in-pull-requests
