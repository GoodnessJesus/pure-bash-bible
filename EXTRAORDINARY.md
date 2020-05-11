<h1 align="center">Extra bash bible</h1> <p
align="center">An extension of pure bash bible.</p>

## Copy a dir include all subdirectories

```sh
cp -r /root/.android /opt/.android
```

## Match whole word

```sh
grep -w target
```

## Print a count of the lines that match a pattern

```sh
grep -c pattern
```

## Execute a command with a time limit

**Example Usage:**
```sh
# timeout sends TERM signal after the 10 seconds. If cmd didn't respond to TERM 
# (e.g. it could block the TERM signal) then timeout sends KILL signal after 5 more seconds.
timeout -k 5 10 cmd
```
