## API Report File for "@backstage/search-common"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
/// <reference types="node" />

import { JsonObject } from '@backstage/types';
import { Readable } from 'stream';
import { Transform } from 'stream';
import { Writable } from 'stream';

// Warning: (ae-missing-release-tag) "DocumentCollatorFactory" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export interface DocumentCollatorFactory {
  getCollator(): Promise<Readable>;
  readonly type: string;
}

// Warning: (ae-missing-release-tag) "DocumentDecoratorFactory" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export interface DocumentDecoratorFactory {
  getDecorator(): Promise<Transform>;
  readonly types?: string[];
}

// Warning: (ae-missing-release-tag) "IndexableDocument" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export interface IndexableDocument {
  location: string;
  text: string;
  title: string;
}

// Warning: (ae-missing-release-tag) "QueryTranslator" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export type QueryTranslator = (query: SearchQuery) => unknown;

// Warning: (ae-missing-release-tag) "SearchEngine" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export interface SearchEngine {
  getIndexer(type: string): Promise<Writable>;
  query(query: SearchQuery): Promise<SearchResultSet>;
  setTranslator(translator: QueryTranslator): void;
}

// Warning: (ae-missing-release-tag) "SearchQuery" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface SearchQuery {
  // (undocumented)
  filters?: JsonObject;
  // (undocumented)
  pageCursor?: string;
  // (undocumented)
  term: string;
  // (undocumented)
  types?: string[];
}

// Warning: (ae-missing-release-tag) "SearchResult" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface SearchResult {
  // (undocumented)
  document: IndexableDocument;
  // (undocumented)
  type: string;
}

// Warning: (ae-missing-release-tag) "SearchResultSet" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface SearchResultSet {
  // (undocumented)
  nextPageCursor?: string;
  // (undocumented)
  previousPageCursor?: string;
  // (undocumented)
  results: SearchResult[];
}
```