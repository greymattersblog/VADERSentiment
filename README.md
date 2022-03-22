# VADERSentiment
The original VADER (Valence Aware Dictionary and sEntiment Reasoner) Python tool and its use can be found here: https://github.com/cjhutto/vaderSentiment

There is a node.js translation of the tool here: https://github.com/nimaeskandary/vaderSentiment-js

There's a CDN version available here: https://github.com/leimapapa/vaderSentiment.js

This version is updated and revised not only for vanilla client-side Javascript, but to work in compatible tools, including Google Apps Script.

This is basically the leimapapa version with a few changes:

- vader.js and vader_lexicon.js are now merged into a single file (no need for export)
- const LEXICON = lexicon line added for compatibility
- calls to SentimentIntensityAnalyzer have been changed to new instances of SentimentIntensityAnalyzer() class
- polarity_scores = (text) => { arrow function changed to polarity_scores(text) { for compatibility with Google Apps Script

Installation:
'''HTML
<script src="path/to/vader.js"></script>
'''

Example usage:
'''JavaScript
const sent = new SentimentIntensityAnalyzer();

console.log(sent.polarity_scores('Hello, world. I am terrible.'));
// {neg: 0.508, neu: 0.492, pos: 0, compound: -0.4767}
'''