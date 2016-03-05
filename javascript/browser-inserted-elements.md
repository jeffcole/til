When using jQuery to get elements, you might sometimes not be getting the element you think you're getting. The browser may insert `tr` within your `thead`, so when you think you're getting the first `tr` in `tbody`, you're actually getting the phantom `thead` `tr`.

[2013-10-31]
