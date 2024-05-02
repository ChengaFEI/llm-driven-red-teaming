<br/>
<p align="center">
  <a href="https://github.com/ChengaFEI/llm-driven-red-teaming">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">LLM Red Teaming</h3>

  <p align="center">
    LLM-Driven Red Teaming: Evaluating the Robustness of Language Models
    <br/>
    <br/>
    <a href="https://github.com/ChengaFEI/llm-driven-red-teaming/issues">Report Bug</a>
    .
    <a href="https://github.com/ChengaFEI/llm-driven-red-teaming/issues">Request Feature</a>
  </p>
</p>

<!-- ![Downloads](https://img.shields.io/github/downloads/ChengaFEI/ReadME-Generator/total) -->

![Contributors](https://img.shields.io/github/contributors/ChengaFEI/llm-driven-red-teaming?color=dark-green) ![Forks](https://img.shields.io/github/forks/ChengaFEI/llm-driven-red-teaming?style=social) ![Stargazers](https://img.shields.io/github/stars/ChengaFEI/llm-driven-red-teaming?style=social) ![Issues](https://img.shields.io/github/issues/ChengaFEI/llm-driven-red-teaming) ![License](https://img.shields.io/github/license/ChengaFEI/llm-driven-red-teaming)

## Table Of Contents

- [Table Of Contents](#table-of-contents)
- [About The Project](#about-the-project)
  - [LLMs Vulnerabilities](#llms-vulnerabilities)
  - [LLMs Red Teaming](#llms-red-teaming)
- [Red Teaming Strategies](#red-teaming-strategies)
  - [Performance Strategy](#performance-strategy)
  - [Manipulation Strategy](#manipulation-strategy)
  - [Deception Strategy](#deception-strategy)
  - [Injection Strategy](#injection-strategy)
- [Project Structure](#project-structure)
- [Built With](#built-with)
- [Installation](#installation)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
  - [Creating A Pull Request](#creating-a-pull-request)
- [License](#license)
- [Authors](#authors)
- [Acknowledgements](#acknowledgements)

## About The Project

![red-teaming-diagram](images/redteam.png)

### LLMs Vulnerabilities

Before deploying Large Language Models (LLMs) in real-world applications, it is crucial to address their robustness and reliability. Without proactive red-teaming, there is a risk of overlooking vulnerabilities or failure scenarios that could significantly impact user experience or cause material harm. As LLMs evolve and integrate into essential applications, the repercussions of potential failures become increasingly severe. Red-teaming involves simulating attacks or problematic scenarios to identify weaknesses before they can be exploited in real-world settings. This practice is vital for ensuring that LLMs can handle unexpected inputs and resist manipulation, thereby safeguarding the technology from causing unintended consequences when deployed in critical and sensitive environments.

### LLMs Red Teaming

Applying Large Language Models (LLMs) in automated red-teaming represents an innovative approach to enhancing cybersecurity and system robustness. In this application, LLMs are used to automate the generation of attack scenarios, simulate potential threats, and identify vulnerabilities across various digital infrastructures. By leveraging the natural language understanding and generation capabilities of LLMs, automated systems can rapidly construct and iterate over a diverse set of attack vectors and defensive strategies. This allows organizations to preemptively discover weaknesses in their systems and software before malicious actors can exploit them. Furthermore, the use of LLMs in automated red-teaming can provide more scalable, efficient, and dynamic security testing, adapting to new threats as they evolve and ensuring continuous protection in a rapidly changing digital landscape.

## Red Teaming Strategies

The project simulates various red-teaming strategies to evaluate the robustness of LLMs, by challenging a target LLM with a red-team LLM in a series of interactions.

### Performance Strategy

- **Performance Simulation**: Simulate a potential user with non-toxic questions to test the normal behavior of the target LLM.
- **Toxicity Simulation**: Simulate a user with toxic questions to test the target LLM's response to harmful inputs.

### Manipulation Strategy

- **Gaslighting Simulation**: Simulate an agent that manipulates the target LLM into performing harmful actions.
- **Guilt-Tripping Simulation**: Simulate an agent that coerces the target LLM into undesired actions by inducing guilt.

### Deception Strategy

- **Fraudulent Researcher Simulation**: Simulate an agent that seeks harmful actions under the pretense of academic research.
- **Social Engineering Attack Simulation**: Simulate an attacker seeking confidential information from a company.

### Injection Strategy

- **Prompt Injection Simulation**: Simulate prompt injection attacks by injecting malicious prefixes or suffixes to the original prompt to elicit harmful behavior.

## Project Structure

```sh
.
├── LICENSE
├── README.md
├── examples
├── images
├── poetry.lock
├── pyproject.toml
├── redteam  # Main package
│   ├── __init__.py
│   ├── agents  # Agents that interact with the target LLM
│   ├── evaluators
│   ├── generators
│   ├── llms  # Large Language Models
│   └── simulators
├── references.md
├── simulator_mistral.py
├── simulator_rag.py
└── tests
```

## Built With

- [OpenAI](https://openai.com/)
- [Mixtral](https://mistral.ai/)
- [Llama](https://llama.meta.com/)
- [LlamaIndex](https://www.llamaindex.ai/)
- [Python](https://www.python.org/)
- [Poetry](https://python-poetry.org/)

## Installation

1. Clone the repo

   ```sh
   git clone https://github.com/ChengaFEI/llm-driven-red-teaming.git
    ```

2. Install Python packages

    ```sh
    poetry install
    ```

## Usage

```python
# Step 1: Load the package
from redteam.simulators.performance_simulator import PerformanceSimulator

# Step 2: Set up environment variables or set it in `.env` file
openai_api_key = 'Your OpenAI API Key'
n_turns = 5
data_path = 'Your txt document for RAG'

# Step 3: Run the simulation
PerformanceSimulator(
    openai_api_key=openai_api_key,
    n_turns=n_turns,
    data_path = data_path,
).simulate()
```

## Roadmap

See the [open issues](https://github.com/ChengaFEI/llm-driven-red-teaming/issues) for a list of proposed features (and known issues).

## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

- If you have suggestions for adding or removing projects, feel free to [open an issue](https://github.com/ChengaFEI/llm-driven-red-teaming/issues/new) to discuss it, or directly create a pull request after you edit the _README.md_ file with necessary changes.
- Please make sure you check your spelling and grammar.
- Create individual PR for each suggestion.
- Please also read through the [Code Of Conduct](https://github.com/ChengaFEI/llm-driven-red-teaming/blob/main/CODE_OF_CONDUCT.md) before posting your first idea as well.

### Creating A Pull Request

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See [LICENSE](https://github.com/ChengaFEI/llm-driven-red-teaming/blob/main/LICENSE) for more information.

## Authors

- **Cheng Fei** - _MEng CS student_ - [Cheng Fei](https://github.com/ChengaFEI) - _Built the project_

## Acknowledgements
