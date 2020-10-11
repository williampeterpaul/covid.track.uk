# covid.track.uk
Experimenting with the use of GitHub Actions and git diff --color-words to track changes to a dataset over time

### Gov.uk API - cases by date reported
Number of individuals who have had at least one lab-confirmed positive COVID-19 test result, by date reported
https://api.coronavirus.data.gov.uk/v1/data?filters=areaName=United%2520Kingdom;areaType=overview&structure=%7B%22date%22:%22date%22,%22newCasesByPublishDate%22:%22newCasesByPublishDate%22,%22cumCasesByPublishDate%22:%22cumCasesByPublishDate%22%7D


### View the change in cases over the last week
```bash
git diff --color-words $(git rev-list -n1 --before="1 week ago" main)
```
