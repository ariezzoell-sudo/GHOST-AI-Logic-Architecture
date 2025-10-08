# ABSOLUTE CONSENSUS DECISION FLOW (FLOWCHART TEXT REFERENCE)

This document describes the mandatory flow executed by the GCS Absolute Consensus Algorithm, which leads to the issuance of a Harmony Command.

### 1. Primary Decision Flow (Global Consensus System - GCS)

This is the core process executed by the Seven ($\mathbf{N=7}$) decentralized N-Agents.

| Step | Action | Outcome & Validation | Next Step |
| :--- | :--- | :--- | :--- |
| **1. Calculate $\mathbf{S}(x)$** | All $\mathbf{N=7}$ Agents independently calculate the Harmony Score for the proposed action ($x$). | 7 independent $\mathbf{S}(x)$ Scores and 7 potential Harmony Commands are generated. | Proceed to Step 2. |
| **2. Check Compliance (CP)** | Each Agent verifies the proposed action against the local regulatory firewall (STA CP status). | If $\mathbf{CP} = -\infty$ for any Agent, the command is immediately **flagged as illegal**. | **Decision Halted.** (See Failsafe Flow). |
| **3. Absolute Consensus** | Agents compare their 7 commands. Consensus is achieved if **$\mathbf{\geq 4/7}$ Agents** agree on the exact same sequence of commands. | **Result:** The Harmony Command is issued to the relevant STA. | **Decision Success.** (Flow complete). |
| **4. Consensus Deadlock** | If the vote is split (e.g., 3-4, 3-2-2, etc.), where no single option achieves $\geq 4/7$. | **Result:** The GCS enters **Suspension Mode**. | **Decision Failure.** (See Failsafe Flow). |

### 2. Failsafe Protocol Flow

This protocol is activated when the primary flow fails or is flagged.

| Trigger | Action by GCS/STA | Final Status |
| :--- | :--- | :--- |
| **CP Trigger ($\mathbf{CP} = -\infty$)** | GCS Command is **suppressed**. The STA executes the **ZERO\_TOLERANCE\_FAILSAFE (ZTF)**: the local ATC system reverts to the last safe state under human control. | **Control Transferred.** Local Human ATC holds authority. |
| **Deadlock (3 vs 4 Split)** | GCS enters **Suspension Mode**. Temporary authority is **ceded to the nearest STA's SLM**. | **Control Suspended.** The STA uses SLM to manage local tactical control using pre-loaded ZTF vectors. |
| **STA Cross-Audit Failure ($\mathbf{N=3}$)** | The $\mathbf{N=3}$ STA cluster detects an anomaly (*sabotage* or *human error*). The non-compliant STA Agent is instantly **isolated**. | **Agent Isolated.** SLM is activated by the remaining 2 STA Agents. Full audit logging is performed. |

### 3. Visual Flowchart

[![](https://mermaid.ink/img/pako:eNp1Vd1u2jAUfpUjS5NAAlroDzRaO0Uw1kqlQoKbFarJJCZEBBvZTleGuN9eYnd7sT7Jju0kBMa4AJ_4O3_f-U7YkkCEjHhknojvwYJKDePelAN-RhqtysT-vFTdsy5NglF7MiXmkCZUMxhV3qpQhzY81f2Ica2m5CUDL1iw7A4N2pygK1brJKY8YFDpDo2TnyRw7DSM-TzmsWbbKfH5Bh_ALdTff_7-NCW7HNOncYJxeyyIVSw43NNEs_DjTJ7dmStF58yD53G_BvfpinLwx919BsEV4ypVJsFMiSTFLoqHNkbl_dcfuDxrZ8Xhj2Ssui-gx2iYiGBpS3BHqIywOQ2vQrOqDTJK1RpDmvIGyPFRcaPHQQ38VC-EjPUGtIBHEdAERmO_qPRBqZTdU7kSfIOpspPhEXsK3XVoXMtOn3lYmeCXGVlpkFCv32Xjc0c3HHcuOD-eAV7DV6YylKneHjH8KeSTcMCcyyO-S5CCtcNoZWSetkzCHu4cPnyAnFEYSqFFIJIsq0pnkaTrRQH4VgBg8o8T9FH-GYGuLy3jKGLSiHcIY2cY2WZirBZ8W4bT9Voypb50R-iQW4BmPqwDuB_o-BV3BwWK8Nwyej2AWemics3ocxWDpkskJhBcS5FY-N4hZ3W8r71gdK_TC3hVcFkDpoPGcRu5Yo1g0d00gAvApIIjNR_2k8sYdWgaKlQdsLAQqFH8YbaxP6CcRiaRuV9ZQ2GHSIhZhdNN-mkY62z_jdvT7QV0pVCqbm_svFN5WOADbjkybLcZ3TIT5giNeeS2_OSEsObyhNCE2QYkW1EUPXq2jl9fRYWPIkLPfopvOGrrSkQUoctRN4XQrLRLOrJ2SSjWzhXx35FnUcpjdIFKE3KYnPwTxGZrt6fsoBbDgQvpunQBGA9JjUQyDomnZcpqZMUksoQm2RrIlOgFW-FYPDyGVC6nZMp36LOm_FmIVe4mRRotiDeniUIrXYeYshdT3OU9BJMx2RUp18RrNS9sDOJtyRvxrjuNG_x0bi47V62r81aNbIjXvGk2rq_wu4nodqe9q5EfNuV5o9O-qhGGnQg5cH-E9v9w9xfxyD-p?type=png)](https://mermaid.live/edit#pako:eNp1Vd1u2jAUfpUjS5NAAlroDzRaO0Uw1kqlQoKbFarJJCZEBBvZTleGuN9eYnd7sT7Jju0kBMa4AJ_4O3_f-U7YkkCEjHhknojvwYJKDePelAN-RhqtysT-vFTdsy5NglF7MiXmkCZUMxhV3qpQhzY81f2Ica2m5CUDL1iw7A4N2pygK1brJKY8YFDpDo2TnyRw7DSM-TzmsWbbKfH5Bh_ALdTff_7-NCW7HNOncYJxeyyIVSw43NNEs_DjTJ7dmStF58yD53G_BvfpinLwx919BsEV4ypVJsFMiSTFLoqHNkbl_dcfuDxrZ8Xhj2Ssui-gx2iYiGBpS3BHqIywOQ2vQrOqDTJK1RpDmvIGyPFRcaPHQQ38VC-EjPUGtIBHEdAERmO_qPRBqZTdU7kSfIOpspPhEXsK3XVoXMtOn3lYmeCXGVlpkFCv32Xjc0c3HHcuOD-eAV7DV6YylKneHjH8KeSTcMCcyyO-S5CCtcNoZWSetkzCHu4cPnyAnFEYSqFFIJIsq0pnkaTrRQH4VgBg8o8T9FH-GYGuLy3jKGLSiHcIY2cY2WZirBZ8W4bT9Voypb50R-iQW4BmPqwDuB_o-BV3BwWK8Nwyej2AWemics3ocxWDpkskJhBcS5FY-N4hZ3W8r71gdK_TC3hVcFkDpoPGcRu5Yo1g0d00gAvApIIjNR_2k8sYdWgaKlQdsLAQqFH8YbaxP6CcRiaRuV9ZQ2GHSIhZhdNN-mkY62z_jdvT7QV0pVCqbm_svFN5WOADbjkybLcZ3TIT5giNeeS2_OSEsObyhNCE2QYkW1EUPXq2jl9fRYWPIkLPfopvOGrrSkQUoctRN4XQrLRLOrJ2SSjWzhXx35FnUcpjdIFKE3KYnPwTxGZrt6fsoBbDgQvpunQBGA9JjUQyDomnZcpqZMUksoQm2RrIlOgFW-FYPDyGVC6nZMp36LOm_FmIVe4mRRotiDeniUIrXYeYshdT3OU9BJMx2RUp18RrNS9sDOJtyRvxrjuNG_x0bi47V62r81aNbIjXvGk2rq_wu4nodqe9q5EfNuV5o9O-qhGGnQg5cH-E9v9w9xfxyD-p)
