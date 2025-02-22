<!--- Hugo front matter used to generate the website version of this page:
--->

<!-- NOTE: THIS FILE IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/attribute_namespace.md.j2 -->

# CICD

## CI/CD Pipeline Attributes

This group describes attributes specific to pipelines within a Continuous Integration and Continuous Deployment (CI/CD) system. A [pipeline](https://wikipedia.org/wiki/Pipeline_(computing)) in this case is a series of steps that are performed in order to deliver a new version of software. This aligns with the [Britannica](https://www.britannica.com/dictionary/pipeline) definition of a pipeline where a **pipeline** is the system for developing and producing something. In the context of CI/CD, a pipeline produces or delivers software.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="cicd-pipeline-name" href="#cicd-pipeline-name">`cicd.pipeline.name`</a> | string | The human readable name of the pipeline within a CI/CD system. | `Build and Test`; `Lint`; `Deploy Go Project`; `deploy_to_environment` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-pipeline-result" href="#cicd-pipeline-result">`cicd.pipeline.result`</a> | string | The result of a pipeline run. | `success`; `failure`; `timeout`; `skipped` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-pipeline-run-id" href="#cicd-pipeline-run-id">`cicd.pipeline.run.id`</a> | string | The unique identifier of a pipeline run within a CI/CD system. | `120912` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-pipeline-run-state" href="#cicd-pipeline-run-state">`cicd.pipeline.run.state`</a> | string | The pipeline run goes through these states during its lifecycle. | `pending`; `executing`; `finalizing` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-pipeline-task-name" href="#cicd-pipeline-task-name">`cicd.pipeline.task.name`</a> | string | The human readable name of a task within a pipeline. Task here most closely aligns with a [computing process](https://wikipedia.org/wiki/Pipeline_(computing)) in a pipeline. Other terms for tasks include commands, steps, and procedures. | `Run GoLang Linter`; `Go Build`; `go-test`; `deploy_binary` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-pipeline-task-run-id" href="#cicd-pipeline-task-run-id">`cicd.pipeline.task.run.id`</a> | string | The unique identifier of a task run within a pipeline. | `12097` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-pipeline-task-run-url-full" href="#cicd-pipeline-task-run-url-full">`cicd.pipeline.task.run.url.full`</a> | string | The [URL](https://wikipedia.org/wiki/URL) of the pipeline run providing the complete address in order to locate and identify the pipeline run. | `https://github.com/open-telemetry/semantic-conventions/actions/runs/9753949763/job/26920038674?pr=1075` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-pipeline-task-type" href="#cicd-pipeline-task-type">`cicd.pipeline.task.type`</a> | string | The type of the task within a pipeline. | `build`; `test`; `deploy` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-system-component" href="#cicd-system-component">`cicd.system.component`</a> | string | The name of a component of the CICD system. | `controller`; `scheduler`; `agent` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| <a id="cicd-worker-state" href="#cicd-worker-state">`cicd.worker.state`</a> | string | The state of a CICD worker / agent. | `idle`; `busy`; `down` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

---

`cicd.pipeline.result` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `cancellation` | The pipeline run was cancelled, eg. by a user manually cancelling the pipeline run. | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `error` | The pipeline run failed due to an error in the CICD system, eg. due to the worker being killed. | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `failure` | The pipeline run did not finish successfully, eg. due to a compile error or a failing test. Such failures are usually detected by non-zero exit codes of the tools executed in the pipeline run. | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `skip` | The pipeline run was skipped, eg. due to a precondition not being met. | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `success` | The pipeline run finished successfully. | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `timeout` | A timeout caused the pipeline run to be interrupted. | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

---

`cicd.pipeline.run.state` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `executing` | The executing state spans the execution of any run tasks (eg. build, test). | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `finalizing` | The finalizing state spans from when the run has finished executing (eg. cleanup of run resources). | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `pending` | The run pending state spans from the event triggering the pipeline run until the execution of the run starts (eg. time spent in a queue, provisioning agents, creating run resources). | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

---

`cicd.pipeline.task.type` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `build` | build | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `deploy` | deploy | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `test` | test | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

---

`cicd.worker.state` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `available` | The worker is not performing work for the CICD system. It is available to the CICD system to perform work on (online / idle). [1] | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `busy` | The worker is performing work for the CICD system. | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `offline` | The worker is not available to the CICD system (disconnected / down). | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** Pipelines might have conditions on which workers they are able to run so not every worker might be available to every pipeline.
