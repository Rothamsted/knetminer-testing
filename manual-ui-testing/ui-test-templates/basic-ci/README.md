# [BasicCI] Basic tests, local instance

[Test instances][TPLINST]

## Initial loading
* Go to https://knetminer.com/ci-test/client/
* [ ] The initial screenshot loads correctly, including the "share your feedback banner"
  * [ ] If that doesn't work, try http://babvs73.rothamsted.ac.uk:9100/client/. If that only works,
        it's likely to be a web proxy configuration, report a failure and continue with this URL.
* [ ] The Javascript console doesn't show errors
* [ ] Check the `Release Notes Icon`
* [ ] Check the other links on the top: tutorial, cite us. For sign-in, sign-up, verify the inital forms appears. There is another test TODO about interacting with knetspace.

## Testing the Examples

### Click on "Keyword search (AND)"
* [ ] `Keywords` field is populated with: `"seed germination" AND flavon*`
* [ ] Under keywords, it shows: `16 documents and 215 genes will be found with this query`
* [ ] The other fields are empty
* [ ] Leave the keyword field with just `seed germination`, counts increase to
      1745 documents and 7934 genes
* Click on `Search`
* [ ] After a few secs, something like `In total In total 7934 genes were found (2.30 seconds).` is
      shown at the bottom of the search form
* [ ] The same no. of genes is shown in the gene table. Check it matches [this](TODO)
* [ ] Switch to the evidence view. It matches [this](TODO)
* [ ] Click on the map view, check it matches [this](TODO) (we're aware of the 
      graphic glitch on the bottom
* [ ] Go back to the gene view, select the first 3 genes, `3 genes selected` should appear 
      click on `Create network view`. Check it matches [this](TODO)
* Check net view functionality
* [ ] Clicking and dragging on a blank point. the graph moves
* [ ] Right-click on a node, the options wheel appears
* [ ] From the option wheels, it's possible to show the info box on the right, this seems fine
* [ ] The info box works for other nodes and edges
* [ ] Other option wheels options work
* [ ] The info box can be closed (we're aware that sometimes you need the enlarged view for this)
* [ ] The info box can be opened/closed with the top icon. We're aware it's initially empty and it's only emptied on second click, not closed.
* [ ] In the legend, click on CellComp (or other node). New nodes should show up. Double click on the same icon, the corresponding nodes should disappear.
* [ ] Click on the redraw icon, it should redraw and reposition newly added nodes
* Check other net view options
  * [ ] At least one different layout
  * [ ] `Labels:`
  * [ ] `Label Size`
* [ ] At the end, check the Javascript console for errors
* [ ] At the bottom of the search form, check that `Clear Search Fields` work and that you can use the cleared form again


### Select the example TODO
* [ ] Check it matches [this](TODO)
* [ ] In the Chromosome Region section, check that changing chromosome changes count
* [ ] Check add/remove chromosome regions
* Search with the initial region
* [ ] Check [the gene view](TODO)
* [ ] Check the [evidence view](TODO), check it has p-values, downloadable genes, 
      gene list (click and verify links)
       **WARNING**: we already know Js doesn't have access to the browser clipboard (eg, in Chrome), when you're testing an URL like `http://babvs*`, due to the fact it's not https and not 
      considered secure ([ref](https://stackoverflow.com/questions/51805395)).
* [ ] Check the chromosome view, the chromosome 1 should be plenty of entries
* [ ] Check the chromosome view: resize, redraw, auto-labels, genes number, save, advanced options
* [ ] Select a few genes on the chromosome view, click on the net view icon on the top left, verify 
      a net view appears
* [ ] At the end, check the Javascript console
      
## Switching specie
* [ ] The specie selector on the top left switches between species, changing examples correctly
      (1 ex for Triticum, 2 for Zea)
* [ ] Do similar tests to the above, verifying the examples work for the other species too

## Misc UI tests
* [ ] In the gene view, clicking on a single gene shows its network view
* [ ] In the `Keywords`, when you start typing, the counter down the text box changes
* [ ] The concept selector on the end of `Keywords` works fine (including +/-)
* [ ] The concept selector is blanked when the `Keywords` box is emptied
* [ ] In evidence view -> `Genes`, click on a row, the copy and donwload buttons work fine.
      Paste some list in the search box. 
      **WARNING**: again, we already know Js doesn't have access to the browser clipboard (eg, in Chrome), when you're testing an URL like `http://babvs*`, due to the fact it's not https and not 
      considered secure ([ref](https://stackoverflow.com/questions/51805395)).
* [ ] In the evidence view, clicking on `Gene list` show the network view for those user genes.
      It might take a while and without progressing messages.

## URL-related tests
* [ ] Go to go to https://knetminer.com/ci-test/client/?taxId=4565
      The UI opens with *Triticum Aestivum* selected
* [ ] Go to this [/genome URL](https://knetminer.com/ci-test/ws/wheatknet-beta/genome?keyword=flowering%20FLC%20FT&list=TRP*,BRA*). A correct reply is given.
* [ ] Go to this [/genome URL](https://knetminer.com/ci-test/ws/genome?keyword=flowering%20FLC%20FT&list=TRP*,BRA*), which omits the data source ID from the URL. A correct reply is given.

## Gene page test
* [ ] This [gene page URL](http://localhost:8080/html/genepage.jsp?keywords="cold%20tolerance"&list=TPP1,TPP4,TPPE)  works correctly.


## Headline for the test instances

**Please, report this Markdown code at the beginning of every GH ticket that represents a report on running the test described in the hereby template**:

```Markdown
*This is a manual UI test based on [this template][TPLREF]. Other instances of this test are [here][TPLREF]. Tests from the template that aren't mentioned hereby are intended as passed.*

[TPLREF]: https://github.com/Rothamsted/knetminer-testing/blob/v2.1/manual-ui-testing/ui-test-templates/basic-ci/README.md
[TPLINST]: https://github.com/Rothamsted/knetminer/issues?q=BasicCI
```

**Please, when opening an issue about this test, always use this format**:

```
[BasicCI UI Test] <description>
```

This is useful to [find test instances][TPLINST] from the template.

[TPLREF]: https://github.com/Rothamsted/knetminer-testing/blob/v2.1/manual-ui-testing/ui-test-templates/basic-ci/README.md
[TPLINST]: https://github.com/Rothamsted/knetminer/issues?q=BasicCI

