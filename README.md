# autoblack

### GitHub Action that uses Black to reformat the Python code in incoming pull requests.

If all Python code in a pull request is already Blackened then this Action gives the PR a ✅ and does nothing else.

Otherwise, Blackened code is _committed back_ to that pull request.

This means that no pull request will have passing tests until its code is Blackened and that reformatting is _automatic_ with no pre-commit hooks, etc.

Inspired by:
* https://github.com/lgeiger/black-action/pull/2
* https://peterevans.dev/posts/github-actions-how-to-automate-code-formatting-in-pull-requests

### tl;dr: It does not work.

> After poking around a bit, it seems to be a design decision by the GitHub Actions team that the GitHub Actions bot can't push to either repo on a pull request from fork.

See [this comment from @chrispat](https://github.community/t5/GitHub-Actions/Can-t-push-to-forked-repository-on-the-original-repository-s/m-p/35916/highlight/true#M2372).

### How can I try it out?
1. [Edit the `platform_info.py` file in this repo](https://github.com/cclauss/autoblack/edit/master/platform_info.py).
2. Make a change that contains Python code which is not Blackened.
3. Submit that change as a pull request.
4. This Action should run and reformat the code to be Black compliant and commit that to your pull request.

[.github/workflows/reblack.yml](.github/workflows/reblack.yml)

In no way related to https://www.urbandictionary.com/define.php?term=autoblack
