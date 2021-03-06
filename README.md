# Autocomplete-Trie

Trie data structure exercise


## Working on the exercise

Review the code in `./test/` directory to understand how your functions will be used.

Do all your work in `./trie.js`, more explanations will be in that module.

### trie.create

Work on this first. This function will take in a dictionary, and output a trie data structure.

Check your work on a small sample dictionary using `npm run test:create`
Alternatively, you can use [`nodemon`](https://www.npmjs.com/package/nodemon) for rapid development: `npx nodemon test/create`

See [./test/sample-dictionary.json](./test/sample-dictionary.json) for an example.


### trie.check

Work on this next. `trie.check` relies on `trie.create`. This function will take in a dictionary, and output a trie data structure.

Check your work on a small sample dictionary using `npm run test:create`
Alternatively, you can use [`nodemon`](https://www.npmjs.com/package/nodemon) for rapid development: `npx nodemon test/create`


See [./test/sample-trie.json](./test/sample-trie.json) for an example.

### test both

Run `npm test` and make sure the output is `"OK!"`

### stretch goals

When all tests pass, see if you can add some features.

**trie.create** write a `trie.add()` function that adds a word to the trie

**trie.create** write a `trie.remove()` function that removes a word from the trie

**trie.check** adjust it to also decorate the `node.value` with `node.suggestions` which returns an array of possible words that are one level deep in the node's children.

**trie.check** memoize the function to cache results which will make walking a down the trie faster.

## Running the app

This should only be done when tests pass.

Run `npm start` to run the demo app.

`open localhost:3000` to launch and interact with it.

## Dictionary

The dataset is a giant json document that looks like this
```json
{
  "predominance" : {
    "word": "predominance",
    "wordset_id": "54bd57017265742391c2fe03",
    "meanings": [
      {
        "id": "54bd57017265742391c4fe03",
        "def": "the quality of being more noticeable than anything else",
        "speech_part": "noun",
        "synonyms": [
          "predomination"
        ]
      },
      {
        "id": "54bd57017265742391c5fe03",
        "def": "the state of being predominant over others",
        "speech_part": "noun",
        "synonyms": [
          "predomination"
        ]
      }
    ]
  }
}
```
## Utils

Utilities for curriculum developers.

These scripts are meant to be run in the `data/` directory from this repo [github.com/wordset/wordset-dictionary](https://github.com/wordset/wordset-dictionary)

```sh
./utils/compress.js
```

Will read all json files, except for `misc.json`, compile them into a single json, compresses it, then saves it to `dictionary.json.gz`


```sh
./utils/decompress.js
```

Will read `dictionary.json.gz`, decompress it, parse the json, and displays a random entry in the dictionary.
