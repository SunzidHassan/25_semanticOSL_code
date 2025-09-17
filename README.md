# Semantic Odor Source Localization via Visual and Olfactory Integrated Navigation
> Code release for our IEEE AIRC publication.

[Project page](https://sunzidhassan.github.io/25_semanticOSL/) | [Paper](https://ieeexplore.ieee.org/document/11077500)

[Lingxiao Wang](https://lingxiaow.github.io/index/) |
[Sunzid Hassan](https://sunzid.com/) |
[Khan Raqib Mahmud](https://scholar.google.com/citations?user=g64GPuIAAAAJ&hl=en) |


## 🔍 Framework Overview
<p align="center">
	<img src="assets/LLMFlow2.png" />
</p>
Odor Source Localization (OSL) technology allows autonomous agents like mobile robots to find an unknown odor source in a given environment. Our proposed semantic OSL navigation algorithm integrates visual and olfactory sensing with LLM reasoning to infer likely odor sources and guide robot navigation. Simulation results show improved success rates and shorter travel distances compared to random walk, vision-only, and olfaction-only approaches.

## 🚀 Getting Started
### 1. Requirements

We recommend setting up a python virtualenv or conda environment to help manage dependencies. Our code has been tested primarily with Python 3.10.

Sample instruction for `conda` users.
```bash
conda create --name sosl python=3.10
conda activate sosl
pip install -r requirements.txt
```

### 2. Configuration ⚙️ 
All configurable parameters are located in `config.yaml`.

Before running the algorithm, make sure to set up your OpenAI API keys. Please note that using the OpenAI API will incur costs ($$$).

Configure as below in `config.yaml`:
```yaml
OPENAI_KEY: # 'sk-xxxxxx' 
OPENAI_CHAT_MODEL: 'gpt-4o'
```
[Alternative Models](https://platform.openai.com/docs/models)

### 3. Running the Program
Running the navigation algorithm is straightforward:
```bash
python sOSL_iThor_nav03.py #for vision and olfaction fusion algorithm
python sOSL_iThor_nav03_VO.py #for vision-only algorithm
python sOSL_iThor_nav03_OO.py #for olfaction-only algorithm
python sOSL_iThor_nav03_RW.py #for random-walk algorithm

```

The program will save robot's egocentric frames, and a csv file containing LLM reasoning output. Check the `save` directory for sample output.

## 🔖 Citation
`
@inproceedings{wang2025semantic,
                title={Semantic Odor Source Localization via Visual and Olfactory Integrated Navigation},
                author={Wang, Lingxiao and Hassan, Sunzid and Mahmud, Khan Raqib},
                booktitle={2025 6th International Conference on Artificial Intelligence, Robotics and Control (AIRC)},
                pages={87--93},
                year={2025},
                organization={IEEE}
              }
`
