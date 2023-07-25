# metaphor-node

Our official Node SDK. Uses axios under the hood.

https://www.npmjs.com/package/metaphor-node

## Installation
```
npm install metaphor-node
```

### `metaphor.search(query: string, options?: SearchOptions): Promise<SearchResponse>`
Performs a search on the Metaphor system with the given parameters.

```javascript
const response = await metaphor.search('global warming', {
  numResults: 5,
  includeDomains: ['example.com'],
});
```

### `metaphor.findSimilar(url: string, options?: FindSimilarOptions): Promise<SearchResponse>`
Finds content similar to the specified URL.

```javascript
const response = await metaphor.findSimilar('https://example.com/some-article', {
  numResults: 3
});
```

### `metaphor.getContents(ids: string[] | Result[]): Promise<GetContentsResponse>`
Retrieves the contents of the specified documents.

```javascript
const response = await metaphor.getContents(['doc1', 'doc2']);
```

# Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.
