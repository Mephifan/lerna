# `@lerna/describe-ref`

> Parse [git describe][] output for lerna-related tags

## Usage

```js
const describe = require('@lerna/describe-ref');

(async () => {
  const { lastTag, lastVersion, refCount, sha, isDirty } = await describe();
})();

// values listed here are their defaults
const options = {
  cwd: process.cwd(),
  // pass a glob to match tag name, e.g. "v*.*.*"
  match: undefined,
};

const {
  lastTag,
  lastVersion,
  refCount,
  sha,
  isDirty,
} = describe.sync(options);

const result = describe.parse("v1.0.0-5-gdeadbeef");
// { lastTag, lastVersion, refCount, sha, isDirty }
```

[git describe]: https://git-scm.com/docs/git-describe