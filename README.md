# venture-miner

Mine alphaXiv research breakthroughs, match them to real market pain, and emit scored startup opportunity briefs.

> **Status: early development.** The project is scaffolded; the pipeline is not implemented yet.

## Idea

Academic breakthroughs are described in theoretical terms; market problems show up as messy, practical complaints. venture-miner bridges the two:

- **Supply:** trending alphaXiv papers, author Q&A, and linked code, deconstructed into the core capability unlock (cost, speed, or accuracy delta).
- **Demand:** pain points from Reddit, Hacker News, Stack Overflow, GitHub issues, and low-star software reviews, reduced to the underlying constraint and its economic cost.
- **Match:** a functional-constraint prefilter pairs papers with problems, so only a small candidate set needs judging.
- **Score:** each pairing is scored on moat, wedge, feasibility, and market size, then written up as a brief.

Planned shape: a Claude Code skill backed by a thin, deterministic Python scripts layer. Code fetches and filters; the model judges.

## Principles

- **Bring your own key.** The project ships adapters, never credentials. Sources that need a key read it from your environment and report "key missing" when it is absent.
- **Own the data.** venture-miner keeps its own SQLite database and never writes to other tools' stores.

## Development

Requires Python 3.12+ and [uv](https://docs.astral.sh/uv/).

```bash
uv sync
uv run pytest
uv run ruff check .
```

## License

[MIT](LICENSE)
