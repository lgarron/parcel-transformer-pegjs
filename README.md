# `parcel-transformer-pegjs`

A [PEG.js](https://pegjs.org/) transformer for [Parcel 2](https://medium.com/@devongovett/parcel-2-0-0-alpha-1-is-here-8b160c6e3f7e).

## Setup & Usage

Run:

```console
npm install parcel-transformer-pegjs
```

Add to `.parcelrc`:

```json
{
  // ...
  "transformers": {
    "*.pegjs": ["parcel-transformer-pegjs"]
  }
}
```

Usage:

```js
import { parse } from "./grammar.pegjs"
```

## TypeScript

Here's a simple hack for using this in a TypeScript project:

```typescript
// grammar.js
export { parse } from "./grammar.pegjs";

// grammar.d.ts
export function parse(s: string): OutputType;

// caller.ts
import {parse} from "./grammar"
```
