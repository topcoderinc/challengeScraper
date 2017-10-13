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

4 parameters: rate limit in seconds, actual endpoint, output file

```
challengeScraper 5  https://api.topcoder.com/v3/challenges/?limit=10  output.txt
```
