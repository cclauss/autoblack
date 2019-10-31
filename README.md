# autoblack
### GitHub Action that uses Black to reformat Python code in incoming pull requests.
If all Python code in an incoming pull request is complient with Black then this Action does nothing.

Otherwise, Black is run and a new commit with reformatted code is added to that incoming pull request.

This means that no pull request will have passing tests until its code is Black compliant and that reformatting is automatic.

Inspired by:
* https://github.com/lgeiger/black-action/pull/2
* https://peterevans.dev/posts/github-actions-how-to-automate-code-formatting-in-pull-requests

# How can I try it out?
1. [Edit the `platform_info.py` file in this repo](https://github.com/cclauss/autoblack/edit/master/platform_info.py).
2. Make a change that is not Black compliant.
3. Submit that change as a pull request.
4. This Action should run and reformat the code to be Black compliant and commit that to your pull request.

[.github/workflows/reblack.yml](.github/workflows/reblack.yml)
