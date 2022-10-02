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

- Trailing Space
- Tweet with extra trackers / hashbangs
