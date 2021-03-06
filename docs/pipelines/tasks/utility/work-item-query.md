---
title: Work item query task for Azure Pipelines and TFS 
titleSuffix: Azure Pipelines & TFS
description: Build and release task to ensure the number of matching items returned by a work item query in within the configured threshold in Azure Pipelines and TFS
ms.assetid: F24517BD-FEA2-4EFF-8030-EF441B9C7F67
ms.prod: devops
ms.technology: devops-cicd
ms.topic: reference
ms.manager: douge
ms.author: ahomer
author: alexhomer1
ms.date: 08/24/2018
monikerRange: '>= tfs-2017'
---

# Utility: Query Work Items

![icon](_img/query-work-items.png) &nbsp; Ensure the number of matching items returned by a work item query in within the configured thresholds.

Can be used in only an [agentless job](../../process/server-phases.md) of a release pipeline.

::: moniker range="<= tfs-2018"
[!INCLUDE [temp](../../_shared/concept-rename-note.md)]
::: moniker-end

## Demands

None

::: moniker range="> tfs-2018"
## YAML snippet
[!INCLUDE [temp](../_shared/yaml/QueryWorkItemsV0.md)]
::: moniker-end

## Arguments

| Parameter | Comments |
| --- | --- |
| **Query** | Required. Select a work item query within the current project. Can be a built-in or custom query. |
| **Upper threshold** | Required. Maximum number of matching workitems for the query. Default value = 0 |
| **Lower threshold** | Required. Minimum number of matching workitems for the query. Default value = 0 |
| **Control options** | See [Control options](../../process/tasks.md#controloptions) |

Succeeds if _minimum-threshold_ **&lt;=** _#-matching-workitems_ **&lt;=** _maximum-threshold_

For more information about using this task, see [Approvals and gates overview](../../release/approvals/index.md).

## Open source

This task is open source [on GitHub](https://github.com/Microsoft/vsts-tasks). Feedback and contributions are welcome.
