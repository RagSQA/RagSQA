# RagSQA

A comprehensive bilingual audio-based question answering dataset featuring real-time and knowledge-based queries. RagSQA combines spoken audio with context-dependent questions, enabling research in multimodal reasoning and temporal information retrieval.

The full dataset is available for download [here](https://pan.quark.cn/s/f3282d829b41).

---

## Overview

| | Total | Chinese | English |
|---|---|---|---|
| **Samples** | 6,431 | 2,336 | 4,095 |
| **Audio Duration** | 27.3h | 6.6h | 20.7h |
| **Avg Audio Length** | — | 10.2s | 18.2s |
| **Avg Question Length** | — | ~20 chars | ~83 chars |
| **Avg Answer Length** | — | ~6 chars | ~12 chars |
| **Real-time Queries** | 1,319 (20.5%) | 880 (37.7%) | 439 (10.7%) |
| **Non-real-time Queries** | 5,112 (79.5%) | 1,456 (62.3%) | 3,656 (89.3%) |

---

## Dataset Statistics

### Chinese — By Category

| Category | Count | Avg Q Len | Avg A Len | Real-time | Non-real-time |
|---|---|---|---|---|---|
| Daily | 343 | 21 chars | 6 chars | 186 (54.2%) | 157 (45.8%) |
| Sports and Competitions | 399 | 20 chars | 6 chars | 144 (36.1%) | 255 (63.9%) |
| History and Culture | 499 | 20 chars | 6 chars | 195 (39.1%) | 304 (60.9%) |
| Company and Products | 408 | 21 chars | 6 chars | 132 (32.4%) | 276 (67.6%) |
| Professional Fields | 277 | 20 chars | 5 chars | 95 (34.3%) | 182 (65.7%) |
| Others | 410 | 19 chars | 4 chars | 128 (31.2%) | 282 (68.8%) |

### English — By Category

| Category | Count | Avg Q Len | Avg A Len | Real-time | Non-real-time |
|---|---|---|---|---|---|
| Daily | 768 | 80 chars | 13 chars | 140 (18.2%) | 628 (81.8%) |
| Sports and Competitions | 327 | 86 chars | 14 chars | 91 (27.8%) | 236 (72.2%) |
| History and Culture | 2,365 | 85 chars | 11 chars | 47 (2.0%) | 2,318 (98.0%) |
| Company and Products | 345 | 82 chars | 14 chars | 91 (26.4%) | 254 (73.6%) |
| Professional Fields | 239 | 80 chars | 13 chars | 57 (23.8%) | 182 (76.2%) |
| Others | 51 | 74 chars | 12 chars | 13 (25.5%) | 38 (74.5%) |

---

## Data Format

Each sample is stored as a JSON object with the following fields:

```json
{
  "audio": "/path/to/audio.wav",
  "label": 1,
  "real-time": 0,
  "lang": "ch",
  "question": "Audio-grounded question (entity anonymized)",
  "golden-question": "Explicit question with entity name filled in",
  "answer": "Ground truth answer",
  "knowledge": "Supporting knowledge passages (1-2 sentences)"
}
```

| Field | Description |
|---|---|
| `audio` | Path to the WAV audio file |
| `label` | Category index (1–6) |
| `real-time` | `1` if the question requires up-to-date information, `0` otherwise |
| `lang` | Language: `ch` (Chinese) or `en` (English) |
| `question` | Question referring to the audio entity implicitly |
| `golden-question` | Question with the entity name made explicit |
| `answer` | Ground truth answer string |
| `knowledge` | Background knowledge relevant to answering the question |

---

## Download

The full dataset (audio + annotations) is available [here](https://placeholder.quark.cn).
