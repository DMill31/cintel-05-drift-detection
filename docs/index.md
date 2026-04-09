# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Your Files** - how to copy the example and create your version
- **Glossary** - project terms and concepts

## Custom Project

### Dataset
The dataset used in this project comes from a system that records operational metrics.

There are two tables with the same columns.  One table contains reference metrics that is the baseline and the other table contains the current data.

The three columns are:

- requests: the number of requests handled

- errors: the number of failed requests

- total_latency_ms: total response time in milliseconds

### Signals
Many signals are created in this project.

To start, the reference average and current average for all three columns are calculated.

Similarly, the reference standard deviation and current deviation for the columns are also calculated.

The difference between the reference average and current average as well as the difference between the reference standard deviation and the current deviation.

The percent change between the reference average and current average.

Lastly, a drifting flag for each column was made to show True if the data was found to be drifting.

### Experiments
Originally, only the mean difference was created.

I added everything with standard deviation and percent change to see a new perspective on the same data.

### Results
Whether it was the mean or standard deviation, we detected drift either way.  This was to be expected after analyzing the data we were looking at.

The mean difference was as follows: REQUESTS - 36.2, ERRORS - 4, LATENCY - 1835

The standard deviation difference was as follows: REQUESTS - 1.42, ERRORS - 0.47, LATENCY - 174.45

The mean percent change was as follows: REQUESTS - 28.22%, ERRORS - 173.91%, LATENCY - 47.85%

### Interpretation
All three columns increased, meaning that the system experienced a uniform shift.

While all columns increased consistently, the spread stayed generally about the same, given the smaller change in standard deviations.

The percent change lets us see exactly how much each mean changed, and errors showed the greatest increase.

In hindsight, percent change for standard deviation should have been calculated as well, I feel that percent change is easier to understand than difference when discussing the entire system.

## Additional Resources

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)
