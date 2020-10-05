# Azure Pipeline Formats
For use with the Azure DevOps platform.

## Azure Pipelines A
.
├── azure-pipelines-a.yaml
└── README.md

The simplest form of Azure Pipeline, all stages, jobs, and steps are stored in one YAML file. Well-suited for automation with a fixed scope and strictly defined parameters (eg, dev-stage-prod environments).

## Azure Pipelines B
.
├── azure-pipelines-b.main.yaml
├── azure-pipelines-b.tmpl.yaml
└── README.md

A flexible, albeit "hacky", approach to pipelines targeting one or more endpoints. The template file can store steps that will be executed per variable passed as parameters to the template. Keep in mind that only one unique variable can be passed into the template.

## Azure Pipelines C
.
├── azure-pipelines-c.main.yaml
├── dir1
│   └── azure-pipelines-c.dir1.yaml
├── dir2
│   └── azure-pipelines-c.dir2.yaml
└── README.md

A pipeline suited to multiple endpoints, with a combination of shared and unique stages/jobs.
**Note:** Azure Pipelines cannot manage more than 50 template files in a single pipeline.

## Azure Pipelines D
.
├── azure-pipelines-d.main.yaml
├── dir1
│   └── azure-pipelines-d.dir1.vars.yaml
├── dir2
│   └── azure-pipelines-d.dir2.vars.yaml
└── README.md

Using one pipeline, different sets of variables can be used depending on predefined conditions.
**Note:** Azure Pipelines cannot manage more than 50 template files in a single pipeline.
