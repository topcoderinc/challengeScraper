#TOPCODER CHALLENGE DETAILS FOR ANALYTICS

The purpose of the code base is to create a little utility that will allow developers to query full details of challenges to help build analytical sets.

## Requirement
- nodejs 6+

## Setup

```
chmod +x challengeScraper
npm i
```

## Run

5 parameters: rate limit in seconds, actual endpoint, output file, starting offset (optional), ending offset (optional).

* if either of starting offset or ending offset is not present, then starting offset and ending offset are set equal.
* If neither of them is present, starting offset and ending offset are set to 0.
* If the challenge url already contains offset as parameter, it is removed.

Sample usage without starting offset and ending offset -
```
challengeScraper 5  "https://api.topcoder.com/v3/challenges/?limit=2"  output.txt
```

Sample Usage with only starting offset (Note: offset from endpoint is removed) -
```
challengeScraper 5  "https://api.topcoder.com/v3/challenges/?limit=2&offset=0"  output.txt 2
```

Sample Usage with both starting and ending offset -
```
challengeScraper 5  "https://api.topcoder.com/v3/challenges/?limit=10&offset=0"  output.txt 0 2

```
