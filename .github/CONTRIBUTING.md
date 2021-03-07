Hi, thank you for your interest in contributing to the PHPCompatibility website! We look forward to working with you.

Aside from a few specific pages, the documentation on the website is automatically generated from the source code of the [PHPCompatibility repository](https://github.com/PHPCompatibility/PHPCompatibility).

The contents maintained in this repository are:
- The pages in the "Using PHPCompatibility" section.
- Site layout and structure.
- CSS customizations.

Pull requests to improve either of these are welcome.

All the sniff and error code related content is auto-generated from a combination of:
- The sniff class docblocks for each sniff in the [PHPCompatibility repo](https://github.com/PHPCompatibility/PHPCompatibility/PHPCompatibility/Sniffs)
- The sniff specific additional documentation (if available) in the [PHPCompatibility repo](https://github.com/PHPCompatibility/PHPCompatibility/PHPCompatibility/Docs)

Improvements to the sniff and error code related content are very welcome, but should be pulled to the [PHPCompatibility repository](https://github.com/PHPCompatibility/PHPCompatibility).


## How the website is generated

This website is a [GitHub Pages](https://docs.github.com/en/github/working-with-github-pages) site using the [Jekyll Site Generator](https://jekyllrb.com/) with the [Liquid template language](https://shopify.github.io/liquid/) with some [Jekyll specific additions to Liquid](https://jekyllrb.com/docs/liquid/).

The website uses the [jekyll-rtd-theme](https://jekyll-rtd-theme.rundocs.io/) using the [rundocs core](https://rundocs.io/) with some site-specific customizations.

The website is automatically updated whenever a commit is pushed to this repository.

[TODO] Whenever a new release of the PHPCompatibility package is tagged, the documentation which is based on the source code of PHPCompatibility is automatically re-generated using the [PHPCS-docs](https://github.com/PHPCSStandards/phpcs-docs) generator package and committed to this repository via a GitHub actions workflow.


## Testing the website locally

* Install a full [Ruby development environment](https://jekyllrb.com/docs/installation/)
* Clone this repository
* Go to the root directory of the clone of this repository
* Run `bundle update`
* Run `bundle exec jekyll serve`
* You should now be able to open the website in your preferred browser at: http://localhost:4000/

For more information, see the [documentation on testing a GitHub Pages site locally](https://docs.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll).


### Typical issues you may run into when testing the site locally

#### The GitHub API credentials you provided aren't valid.

Follow [these instructions](https://github.com/jekyll/github-metadata/blob/master/docs/authentication.md) on getting an access token set up.



