# Debate Agent Project

A multi-agent AI debate system built using [CrewAI](https://crewai.com). It automatically generates arguments for and against controversial topics and determines which side is more convincing.

## Project Workflow

The system consists of three sequential AI agents:

1. **Proponent Agent**: Generates arguments supporting the topic.
2. **Opponent Agent**: Generates arguments opposing the topic.
3. **Judge Agent**: Evaluates both arguments and selects the stronger one.

The generated arguments and decision are saved as markdown files in the `output/` directory:

* `propose.md`: Arguments supporting the topic
* `oppose.md`: Arguments opposing the topic
* `decide.md`: Judge’s final decision and reasoning

## Installation

Make sure Python (>=3.10, <3.14) is installed, then run:

```bash
pip install uv
crewai install
```

Add your OpenAI API key in a `.env` file:

```env
OPENAI_API_KEY=your_openai_api_key
```

## Running the Project

Execute:

```bash
crewai run
```

## Customizing the Topic

Set your debate topic in `src/debate/main.py`:

```python
inputs = {
    'topic': 'Your topic here',
    'current_year': str(datetime.now().year)
}
```

## Configuration

* **Agents**: Adjust agent characteristics in `src/debate/config/agents.yaml`.
* **Tasks**: Modify agent tasks in `src/debate/config/tasks.yaml`.
* **Logic**: Customize workflow logic in `src/debate/crew.py`.

## Output Example

The system provides structured, impartial arguments for complex issues and makes an objective decision based on argument strength.

## Support Resources

* [CrewAI Documentation](https://docs.crewai.com)
* [CrewAI GitHub](https://github.com/joaomdmoura/crewai)
* [CrewAI Discord](https://discord.com/invite/X4JWnZnxPb)

