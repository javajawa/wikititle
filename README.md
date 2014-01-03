# Wiki Title

Simple PHP script for grabbing episode titles out of List of <Series> Episodes
pages on Wikipedia with the Wikipedia API.

## Usage


`wikititle` takes three arguments: the name of the series, the season number,
and the episode number.

```
 $ wikititle "The Simpsons" 10 2
The Wizard of Evergreen Terrace
```

If also scans for one environment variable `WTCACHE`, which can be used to point
to a folder in which wikititle can cache document contents.

```
 $ WTCACHE=/tmp/wikititle ./wikititle Community 4 4
Alternative History of the German Invasion
```

### Output

If the lookup succeeds, the title will be printed to stdout *without* a trialing
new line.

Extra information about errors and pages being downloaded will be sent to stderr.

### Status Codes

- `0` Success
- `1` Data not available
- `2` Wikipedia internal linking issue
