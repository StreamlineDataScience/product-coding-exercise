
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Purpose

This exercise is about data organization, orchestration, and coding,
including creating Docker images.

Aim of this exercise is to:

1.  Evaluate your coding (e.g. data cleaning)
2.  Understand data orchestration capabilities (e.g. Docker)
3.  Understand how you design a solution (overall thinking)

# Exercise

## Data

The data is daily COVID case data from the United States. The data is
located at:
<https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports_us>

which is a series of CSV files, one for each day.

## Instructions

Put code in a public code repository hosted on GitHub, or a private
repository and add `muschellij2` as a collaborator with read access

Once test is completed please share the Github repository URL to hiring
team so they can review your work

## Deliverables

1.  Create a Github repository named `str-challenge`.
2.  Create a [Docker](https://www.docker.com/) image that can read in
    the data from the day before, and compile a report/print out the
    cases for the day before. If the data is not there, print out a
    diagnostic message. If you are using R, you can use the rocker
    images as a base <https://github.com/rocker-org/rocker-versioned2>
3.  Set up GitHub Actions to build this Docker image
4.  In the Docker image, filter rows that are only in the United States,
    take the mean cases (`Confirmed` variable) and deaths (`Deaths`) by
    state, averaging over counties (`Admin2`).
5.  Run a this pipeline on a schedule (daily) using GitHub Actions.
