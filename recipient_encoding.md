# Recipient Encoding

The keys passed in to the `recipients` field are all of the same format:
a "key" which is just 32 bytes of kinda random noise

e.g.

```
<Buffer 47 c8 5e ab fb 50 a3 11 08 3e 45 9f d0 ac 67 d6 70 a6 fc 2b 31 1b 60 83 a5 46 27 02 f7 5b 5d 8f>
```

There are several different source for this. It could be a:
1. group-key
2. key derived for one specific feed
3. a double-ratchet ... for a specific feed


NOTE: we probably don't want (2), only (3) ...

