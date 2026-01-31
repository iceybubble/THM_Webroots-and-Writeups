Room Name: Hip Flask
Room Link: https://tryhackme.com/room/hipflask

```
We know that we are attacking a webserver, however, the entire server is in scope (not just ports 80 and 443), making this effectively a hybrid between a network and a webapp pentest.
```

```
Is the network portion internal or external?
External
```

```
Attempt a zone transfer against the hipflasks.thm domain.

What subdomain hosts the webapp we're looking for?
hipper
```

```
Might as well be able to prove to the client that we've been here (aside from the many screenshots we have been taking).

What is the root user's password hash?
$6$./Fh3mWMsk8X29kq$6CvaDzV7zlXKn1MMQjXtO.abB4/7ecNKBFkQvEWsLkgM8raAZeuSHZurnXG01pqZ4BY2ubk/WgIbo4ee.wnaP0
```

