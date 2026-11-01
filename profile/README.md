# Darkmatter

Darkmatter turns the hardware you already have into one private mesh and runs intelligence across it. Install an outpost on a laptop, a rack, a vehicle or a cloud tenancy, invite the next machine with a single-use code, then send work: the mesh partitions it, routes each piece to the compute best suited to it and brings the results back. Workloads run where the data is generated and move as conditions change.

## What runs on the mesh

| Modality | Workloads |
| --- | --- |
| **Imagery** | Object detection, pattern of life and segmentation over satellite, aerial and drone imagery, partitioned across the mesh so nothing is downsampled. |
| **Video** | Frontier vision models over live and archived video: detection and tracking, re-identification across cameras, activity and anomaly recognition, change detection at native frame rates. |
| **Geospatial** | Map matching, routing and isochrones, spatial joins, line-of-sight analysis, time and distance matrices and clustering, no longer bottlenecked by a model's context window. |
| **Audio** | Multilingual voice activity detection, speaker embeddings, keyword and key phrase extraction, anomaly detection and translation, at the source and in real time. |
| **Time series** | Sensor readings, equipment measurements and demand: anomalies, operating patterns and forecasts, with analysis distributed by time window or asset. |
| **Text** | Documents, messages, reports and knowledge bases turned into entities, summaries and structured records, with results kept connected to their sources. |

## How it works

- **Outpost.** An installation of Darkmatter on a machine you choose. It runs an agent and the console, serves models, joins the services around it and takes work from its peers.
- **Mesh.** A private network of outposts. The outpost that created it admits the others with single-use invitations, and only members of one mesh run each other's work.
- **Jobs.** Describe bulk work in Python, or submit the Ray or Slurm jobs you already have. Darkmatter partitions and routes each job across the mesh to its optimal compute targets: your hardware, ours, or a partner's on the same mesh.
- **Agents, skills and connectors.** Instructions, tools and business logic become reusable skills that every outpost's agent follows, and the agent reaches your enterprise software and data through [connectors](https://github.com/drkm-hq/connectors) and MCP servers.

## Get started

Darkmatter is opening to new teams in waves. Ask for early access at [drkm.ai](https://drkm.ai). Once your account has installer access, one command installs the CLI on an Apple silicon Mac or on x86-64 or ARM64 Linux, and `drkm start` runs your first outpost:

```sh
curl -fsSL https://drkm.ai/install | sh
```

## Contributions

Work we have taken upstream to the projects the mesh runs on.

- **vLLM.** An fp8 e4m3 KV cache for Inkling on SM100 GPUs, halving KV bytes at long context: the [RFC](https://github.com/vllm-project/vllm/issues/54704), the [vLLM pull request](https://github.com/vllm-project/vllm/pull/54705) and the [attention kernel change](https://github.com/vllm-project/tml-fa4/pull/4) it depends on.
- **verl** and **Inkling on Apple silicon.** Contribution packages for faster training rollouts and for running Inkling on Macs are in final review and will be linked here when they open.

## Elsewhere

- [**connectors**](https://github.com/drkm-hq/connectors): the services, tools and MCP servers an outpost can join, how its agent reaches them, and how to ask for the ones you need. We review every request and build the ones that fit into a coming release.
- [**Hugging Face**](https://huggingface.co/DarkmatterLabs): where Darkmatter's models and model cards are published.

Issues and pull requests are welcome on any public repository here.

<sub>© 2026 Darkmatter Labs, Inc.</sub>
