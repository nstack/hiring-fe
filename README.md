# Front-end Hiring Test

## Introduction

The NStack platform is used to run data science workflows. All workflows are comprised of a source of data (for instance, a database or a CSV), one or more steps (such as pre-processing steps, a data science model, or post-processing steps), and end with a sink (a destination that the data is written to, such as a CRM or database).

A representative workflow would be:

| Type | Step  | Description |
| ------------- | ------------- | ------------- |
| Source | CSV of Data  | Our source: CSV a user uploads which contains historical transactional data  |
| Step | Remove Duplicates  | A pre-processing step to remove all duplicate transactions  |
| Step | Churn Model  | A data science model which takes this data and outputs predictions  |
| Step | Bucketing  | A post-processing step which 'buckets' predictions into Low, Medium, and High  |
| Sink | Database  | Our sink: a data warehouse that the predictions will be written to   |

## Background

These workflows run on the backend of NStack, which lives in the cloud and handles all the complexity of orchestration, running steps, and passing around data, but the analysts inside our customers need a way to visualise and edit their workflows, and create new ones. 

Our backend server exposes an API which, given a workflow's id, returns a JSON object which contains the workflow.

## Task

Build a single page application which provides the the ability to upload a JSON object in the same format as the one contained in this repository. This JSON contains information about the workflow, including its graph (i.e. the nodes and edges of the workflow).

Once uploaded, this page should provide a helpful overview of the workflow, including:

- The name and description of the workflow
- A visual representation of the graph
- For any step in the graph that is not a `Source` or a `Sink`, a button to delete that step
- A button to download the JSON of the workflow, which should only be enabled if a change has been made

You can use ether ES6 or Typescript, and any framework or library that you'd like: there are no extra points for rebuilding what could be done more quickly and simply with an existing library. Once you are finished, you can open a PR here.

Any questions at all, do not hesistate to contact us.

Good luck!
