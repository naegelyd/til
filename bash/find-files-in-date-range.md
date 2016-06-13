### Find files in data range

This can be done through the use of the `-newer<time_code>` option in `find`.
The available time codes are:
 * `mt` - modified
 * `at` - accessed
 * `ct` - created/permissions changed

So, given the above, we could search for all files modified since July 4th, 2016 using:

```sh
find . -newermt 2016-07-04 -type f
```

Or, if we wanted all files that have _not_ been modified since July 4th, 2016:

```sh
find . ! -newermt 2016-07-04 -type f
```

Putting them both together, we can find all files modified between the hours of 10:30AM and 1:30PM on July 4th, 2016 using:

```
find . -newermt "20160704 10:30:00" ! -newermt "20160704 13:30:00" -type f
```
