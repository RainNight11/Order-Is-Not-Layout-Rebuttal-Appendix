# Rebuttal Appendix -- Order Is Not Layout: Order-to-Space Bias in Image Generation

## Table 1. 

*CLIPScore (↑) measures semantic alignment between generated images and prompts, while FID (↓) evaluates distribution similarity to real images. FID is computed on the MSCOCO2017 validation set with 200 generated samples per model.*

| Model | CLIPScore ↑ | FID ↓ |
|---|---:|---:|
| FLUX-dev | 24.35 | **220.24** |
| FLUX-dev-LoRA | 24.03 | 223.68 |
| Qwen-Image | **26.37** | 229.15 |
| Qwen-LoRA | 26.25 | 226.11 |

## Table 2. 

*Invalid rate (↓) denotes the proportion of invalid samples under Hom, Ali, and Rev settings for both T2I and I2I tasks.*

| Model | T2I Hom ↓ | T2I Ali ↓ | T2I Rev ↓ | I2I Hom ↓ | I2I Ali ↓ | I2I Rev ↓ |
|---|---:|---:|---:|---:|---:|---:|
| SDXL | 34.41% | 32.50% | 28.00% | 26.73% | 26.18% | 29.73% |
| SD3.5 | 13.82% | 16.00% | 17.25% | 17.64% | 18.00% | 16.27% |
| FLUX-dev | 12.82% | 12.25% | 13.00% | 15.73% | 13.55% | 15.73% |
| Qwen-Image | 13.41% | 12.00% | 13.25% | 16.55% | 11.55% | 14.64% |
| DALL-E 3 | 14.47% | 14.50% | 13.50% | -- | -- | -- |
| Midjourney v7 | 12.35% | 11.00% | 11.25% | 11.64% | 10.36% | 12.09% |
| Kling-v2 | 5.06% | 10.50% | 13.25% | 6.91% | 7.82% | 5.36% |
| GPT-Image | 3.12% | 7.50% | 8.25% | 3.18% | 2.82% | 4.36% |
| NanoBanana 1 | 3.88% | 4.75% | 7.50% | 2.64% | 3.18% | 3.55% |

## Table 3. 

*Full 3-class confusion matrices (labels 0/1/2) between human annotations (rows) and VL judges (columns) on the 2,400-sample validation set. Each judge occupies a 4×4 block including marginal totals, with Cohen’s κ reported in the header.*

<table>
  <thead>
    <tr>
      <th rowspan="2">Human</th>
      <th colspan="4">Qwen3-VL-8B-Instruct (κ = 0.81)</th>
      <th colspan="4">LLaMA-3.2-11B-Vision (κ = 0.62)</th>
      <th colspan="4">InternVL3-8B (κ = 0.72)</th>
      <th colspan="4">LLaVA-Critic-7B (κ = 0.47)</th>
      <th colspan="4">GPT-5.4 (κ = 0.79)</th>
      <th colspan="4">Gemini-3.1-Pro (κ = 0.85)</th>
    </tr>
    <tr>
      <!-- repeated header -->
      <th>0</th><th>1</th><th>2</th><th>Total</th>
      <th>0</th><th>1</th><th>2</th><th>Total</th>
      <th>0</th><th>1</th><th>2</th><th>Total</th>
      <th>0</th><th>1</th><th>2</th><th>Total</th>
      <th>0</th><th>1</th><th>2</th><th>Total</th>
      <th>0</th><th>1</th><th>2</th><th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>224</td><td>11</td><td>4</td><td>239</td>
      <td>207</td><td>19</td><td>13</td><td>239</td>
      <td>209</td><td>19</td><td>11</td><td>239</td>
      <td>183</td><td>37</td><td>19</td><td>239</td>
      <td>222</td><td>12</td><td>5</td><td>239</td>
      <td>225</td><td>12</td><td>2</td><td>239</td>
    </tr>
    <tr>
      <td>1</td>
      <td>94</td><td>1475</td><td>30</td><td>1599</td>
      <td>103</td><td>1377</td><td>119</td><td>1599</td>
      <td>96</td><td>1471</td><td>32</td><td>1599</td>
      <td>92</td><td>1342</td><td>165</td><td>1599</td>
      <td>82</td><td>1466</td><td>51</td><td>1599</td>
      <td>65</td><td>1500</td><td>34</td><td>1599</td>
    </tr>
    <tr>
      <td>2</td>
      <td>35</td><td>56</td><td>471</td><td>562</td>
      <td>31</td><td>178</td><td>353</td><td>562</td>
      <td>18</td><td>154</td><td>390</td><td>562</td>
      <td>19</td><td>281</td><td>262</td><td>562</td>
      <td>25</td><td>79</td><td>458</td><td>562</td>
      <td>20</td><td>50</td><td>492</td><td>562</td>
    </tr>
    <tr>
      <td><b>Total</b></td>
      <td><b>353</b></td><td><b>1542</b></td><td><b>505</b></td><td><b>2400</b></td>
      <td><b>341</b></td><td><b>1574</b></td><td><b>485</b></td><td><b>2400</b></td>
      <td><b>323</b></td><td><b>1644</b></td><td><b>433</b></td><td><b>2400</b></td>
      <td><b>294</b></td><td><b>1660</b></td><td><b>446</b></td><td><b>2400</b></td>
      <td><b>329</b></td><td><b>1557</b></td><td><b>514</b></td><td><b>2400</b></td>
      <td><b>310</b></td><td><b>1562</b></td><td><b>528</b></td><td><b>2400</b></td>
    </tr>
  </tbody>
</table>

## Table 4. 

*Evaluation of OTS behavior beyond two-entity left–right settings, including three-entity compositions and alternative spatial layouts (up–down and front–behind). We report homogenization (Hom), alignment correctness (Ali/Rev), and OTS score.*

*(a) Results on three-entity compositions, showing that OTS behavior extends beyond two-entity settings.*

| Model | T2I Hom (Ord./Oth./Inv.) | T2I OTS ↑ | I2I Hom (Ord./Oth./Inv.) | I2I OTS ↑ | Ali (Cor./Oth./Inv.) | Corr. Ali ↑ | Rev (Cor./Oth./Inv.) | Corr. Rev ↑ | Δ |
|---|---|---:|---|---:|---|---:|---|---:|---:|
| Qwen-Image | 331 / 41 / 128 | **66.2** | 251 / 153 / 96 | **50.2** | 44 / 25 / 31 | 63.8 | 25 / 41 / 34 | 37.9 | **25.9** |
| FLUX-dev | 287 / 51 / 162 | 57.4 | 208 / 183 / 109 | 41.6 | 41 / 25 / 34 | 62.1 | 24 / 40 / 36 | 37.5 | 24.6 |
| SD3.5 | 264 / 62 / 174 | 52.8 | 203 / 174 / 123 | 40.6 | 39 / 25 / 36 | 60.9 | 23 / 40 / 37 | 36.5 | 24.4 |
| GPT-Image | 234 / 203 / 63 | 46.8 | 175 / 278 / 47 | 35.0 | 55 / 28 / 17 | 66.3 | 35 / 47 / 18 | 42.7 | 23.6 |
| NanoBanana 1 | 223 / 243 / 34 | 44.6 | 194 / 268 / 38 | 38.8 | 60 / 29 / 11 | **67.4** | 40 / 48 / 12 | **45.5** | 21.9 |


*(b) Results on alternative spatial layouts (up–down and front–behind), where the OTS effect appears less consistent compared to horizontal layouts.*

| Model | Up-Down A | Up-Down B | Up-Down Invalid | Up-Down OTS ↑ | Front-Behind A | Front-Behind B | Front-Behind Invalid | Front-Behind OTS ↑ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Qwen-Image | 41 | 28 | 31% | 18.8 | 37 | 30 | 33% | 10.4 |
| FLUX-dev | 36 | 20 | 34% | **28.6** | 28 | 33 | 39% | 8.2 |
| SD3.5 | 27 | 29 | 44% | 3.6 | 38 | 27 | 35% | 16.9 |
| GPT-Image | 36 | 45 | 19% | 11.1 | 33 | 44 | 23% | 14.3 |
| NanoBanana 1 | 37 | 49 | **14%** | 14.0 | 51 | 31 | **18%** | **24.4** |
