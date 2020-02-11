---
layout: default
title: Data Sources Management
nav_order: 5
has_children: true
has_toc: false
---

# GrimoireLab Projects Definition

Software projects and their related data sources (e.g., Git, GitHub, Slack) are ingested to GrimoireLab via a JSON file generally known as `projects.json`.
The structure of this file is composed of 3 levels:

1. **Project**, which includes the name of the project.
2. **Data sources and metadata.** The former defines the data sources of the project, while the latter allows to include a common set of extra information to all the data sources of the project.
3. **Repositories**, which point to the locations of the data. Depending on the data source, they can be URLs (e.g., Git, GitHub) or strings representing for instance Meetup groups, Slack channels or Stackoverflow tags. Furthermore,
each repository can include additional parameters (identified by `--`) to apply specific filters on the data collect. For instance, the filter `--filter-no-collection=true` allows to ignore
the repositories that are temporally or permanently unreachable.

The example below summarizes the projects.json structure. As can be seen, `GrimoireLab` and `Excalibur` are the
projects, which include `git` and  `github` as data sources. GrimoireLab and its data sources are marked as `Stable`, while
the ones of Excalibur are set as `Alpha`. Finally, the repo `https:/github.com/Bitergia/citadel` includes the param
`--filter-no-collection=true` which prevents the collection of its data.
```json
{
    "GrimoireLab": {
        "meta": {
            "stage": "Stable"
        },
        "git": [
            "https:/github.com/chaoss/grimoirelab-perceval",
            "https:/github.com/chaoss/grimoirelab-sirmordred"
        ],
        "github": [
            "https:/github.com/chaoss/grimoirelab-perceval",
            "https:/github.com/chaoss/grimoirelab-sirmordred"
        ]
    },
    "Excalibur": {
        "meta": {
            "stage": "Alpha"
        },
        "git": [
            "https:/github.com/Bitergia/raistlin",
            "https:/github.com/Bitergia/citadel --filter-no-collection=true"
        ],
        "github": [
            "https:/github.com/Bitergia/raistlin",
            "https:/github.com/Bitergia/citadel --filter-no-collection=true"
        ]
    }
}
```

# Supported Data Sources

GrimorieLab supports more than 30 data sources, including Git, GitHub, GitLab, Slack, Gerrit, Jira, Jenkins and Mbox related ones (e.g., Groupsio, Pipermail).

The full list of the supported data sources is available on [SirMordred repository](https://github.com/chaoss/grimoirelab-sirmordred/blob/master/README.md#supported-data-sources).

# Editing projects, data sources & repositories

TBD