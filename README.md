This repo contains in-production tests of https://github.com/IstoraMandiri/twitter-together, which is using the Twitter v2 API via https://github.com/twitter-together/action/tree/MattIPv4/twitter-v2-api.

---

## Tweet Types

### Poll

https://github.com/IstoraMandiri/twitter-together-testing/pull/2

```tweet
---
poll:
  - Red
  - Blue
  - Green
---

What is your favorite color?
```

### Reply

https://github.com/IstoraMandiri/twitter-together-testing/pull/3

```tweet
---
reply: https://twitter.com/testing_tt_/status/1576496789741391872
---

You forgot about orange!
```

### Retweet

https://github.com/IstoraMandiri/twitter-together-testing/pull/4

```tweet
---
retweet: https://twitter.com/testing_tt_/status/1576500683087302656
---

Whoops!
```

### Media

https://github.com/IstoraMandiri/twitter-together-testing/pull/5

```tweet
---
media:
  - file: cat.jpg
    alt: A cat
  - file: dog.jpg
    alt: A dog
---

Here are some cute animals!
```

https://unsplash.com/photos/yMSecCHsIBc
https://unsplash.com/photos/Mv9hjnEUHR4

### Threading

https://github.com/IstoraMandiri/twitter-together-testing/pull/6

```tweet
🧵 Here is a thread...

---
---
poll:
  - Banana
  - Mango
---

Which fruit is more delicious?

---
We hope you enjoyed this thread...
---
We certainly did.
```

## Edge Cases

### Trailing Space

https://github.com/IstoraMandiri/twitter-together-testing/pull/7

```tweet
---
retweet: https://twitter.com/testing_tt_/status/1576505043838181377
--- 
```

### URL with Hash

https://github.com/IstoraMandiri/twitter-together-testing/pull/8

PREVIEW PASSING: https://github.com/IstoraMandiri/twitter-together-testing/actions/runs/3168205724

PUBLISH FAILING: https://github.com/IstoraMandiri/twitter-together-testing/actions/runs/3168209652

```tweet
---
retweet: https://twitter.com/testing_tt_/status/1576462993302372355#blah
---
```

### URL with Mock Tracker

https://github.com/IstoraMandiri/twitter-together-testing/pull/9

PREVIEW PASSING: https://github.com/IstoraMandiri/twitter-together-testing/actions/runs/3168218932

PUBLISH FAILING: https://github.com/IstoraMandiri/twitter-together-testing/actions/runs/3168219858

```tweet
---
retweet: https://twitter.com/testing_tt_/status/1576508832418873349?cxt=xxx
---
```

### URL with `mobile` subdomain

https://github.com/IstoraMandiri/twitter-together-testing/pull/9

PREVIEW PASSING: https://github.com/IstoraMandiri/twitter-together-testing/actions/runs/3168231352

PUBLISH FAILING: https://github.com/IstoraMandiri/twitter-together-testing/actions/runs/3168233222

```tweet
---
retweet: https://mobile.twitter.com/testing_tt_/status/1575820698877980672
---
```

### Tweet ID Only

TODO: Not implemented

```tweet
---
retweet: 1575820698877980672
---
```
