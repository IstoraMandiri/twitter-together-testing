Testing https://github.com/IstoraMandiri/twitter-together

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

```tweet
---
reply: https://twitter.com/gr2m/status/1409601188362809349
---

@gr2m I love your work!
```

### Retweet

```tweet
---
retweet: https://twitter.com/gr2m/status/1409601188362809349
---

twitter-together is awesome!
```

### Media

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


### Threading

```tweet
---
media:
  - file: cat.jpg
    alt: A cat
  - file: dog.jpg
    alt: A dog
---

Here are some cute animals!

---
---
poll:
  - Cat
  - Dog
---

Which one is cuter?
```

## Edge Cases

- Trailing Space
- Tweet with extra trackers / hashbangs
