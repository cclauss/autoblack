# autoblack
### GitHub Action that uses Black to reformat Python code in incoming pull requests.
If all Python code in a pull request's branch is already compliant with psf/black then this Action does nothing.

Otherwise, Black reformatted the Python code and those changes are added as a new commit to that pull request.

This means that no pull request will have passing tests until its code is Black compliant and that reformatting is automatic.

Inspired by:
* https://github.com/lgeiger/black-action/pull/2
* https://peterevans.dev/posts/github-actions-how-to-automate-code-formatting-in-pull-requests

### How can I try it out?
1. [Edit the `platform_info.py` file in this repo](https://github.com/cclauss/autoblack/edit/master/platform_info.py).
2. Make a change that is not Black compliant.
3. Submit that change as a pull request.
4. This Action should run and reformat the code to be Black compliant and commit that to your pull request.

[.github/workflows/reblack.yml](.github/workflows/reblack.yml)

In no way related to https://www.urbandictionary.com/define.php?term=autoblack
