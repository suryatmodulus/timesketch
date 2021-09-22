# Concept

Timesketch has a scenario based approach to guide analysts with supportive questions to explore the data set.

Everything below is stored in yaml files to be loaded and easy to edit.

The model is:

```
Scenario --- Investigation 1 --- Question 1
         ``                  --- Question 2
         ``
         --- Investigation 2 --- Question 1
                             --- Question 3
```

## Questions

A single question is by nature small in scope and tactical,
something that can be answered by analysis, either automatically or by
providing enough context so that an analyst can determine the answer.

Each investigation may contain many questions, some dependent on the
outcome of others, that is one question can determine that no further
questions need to be asked,  or that several other questions need to be
brought up, etc.

These questions define what data needs to be present in order to
be able to answer it, as well as what user supplied parameters may be
required to be defined beforehand. It will then also define what set of
analyzers, graph plugins and potential searches will be useful in order
to answer the question and what conditions are sufficient
in order to have the question answered.

As described above, each of these isolated tactical questions are part
of a bigger picture, part of an investigation, which sets out to answer
a broader set of questions, which can then in hand be part of an even
larger scenario.

Each of the questions consist of the following fields:

* display_name
* descriptopm
* data_sources
* parameters
* analyzers

## Investigation

Each investigation have one or more questions to be answered. Each investigaton has a display name and a description.

## Scenario

Each scenario can have multiple investigations.