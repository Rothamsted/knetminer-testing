# [AuthCI] Authentication and Permission Management tests, continuous integration instance

[Test instances][TPLINST]

## Initial loading

As in the [basic test](../basic-ci), [load the CI instance](https://knetminer.com/ci-test/client/) in your browser and verify it shows up

## Authentication

* [ ] Click on "Sign in" on the top right, the sign-in pop-up appears
* [ ] Your KnetSpace credentials work, a successful login message appears and your user name shows up on the header
* [ ] When you click on your user name, a pop-up appears with: Welcome `<username>`, My Profile, My Networks, Email, Organisation
  * [ ] Profile and Networks links lead you to the corresponding KnetSpace pages. If these are wrong, report the problem into the KnetSpace repo, this is a KnetMiner test
* [ ] Go back to KnetMiner, close the user pop-up and re-open it, verify that works, check the Browser's Javascript console doesn't have errors
* [ ] On the user pop-up, click logout, verify the function is working (including clean Js console)


## User Genes limit

Reset the search form.

* [ ] While not logged, start typing random lines in the 'Gene List Search'. The wheel on the right changes its count and appearance accordingly. Try removing lines too
* [ ] Keep adding lines until you have 21 (or the limit reported by the wheel). The wheel becomes red, the Search button is greyed out and disabled
* [ ] Reduce the list back to 20, the wheel is green again and the search button is active again


## Example queries and user management
Load the CI instance as above. 
* [ ] The queries 'Development stages (100 genes)' and 'Shade avoidance (800 genes)' have the '(Login)' annotation.
* [ ] When selecting either, a long list of genes is placed in the Gene List Search box and the right wheel on the box becomes red, as the previous section
* [ ] The other species have similar sample queries

### After login
TODO: new tests to be defined: 
* What should happen to the sample queries? I (MB) have a Pro Plan, but I still see 'Upgrade' links.
* What other restrictions that are unlocked should we test?
* Do we need further test cases about user and permissions?

## Headline for the test instances

**Please, report this Markdown code at the beginning of every GH ticket that represents a report on running the test described in the hereby template**:

```Markdown
*This is a manual UI test based on [this template][TPLREF]. Other instances of this test are [here][TPLINST]. Tests from the template that aren't mentioned hereby are intended as passed.*

[TPLREF]: https://github.com/Rothamsted/knetminer-testing/blob/v3.0/manual-ui-testing/ui-test-templates/auth-ci/README.md
[TPLINST]: https://github.com/Rothamsted/knetminer/issues?q=AuthCI
```

**Please, when opening an issue about this test, always use this format**:

```
[BasicCI UI Test] <description>
```

This is useful to [find test instances][TPLINST] from the template.

[TPLREF]: https://github.com/Rothamsted/knetminer-testing/blob/v3.0/manual-ui-testing/ui-test-templates/auth-ci/README.md
[TPLINST]: https://github.com/Rothamsted/knetminer/issues?q=AuthCI
