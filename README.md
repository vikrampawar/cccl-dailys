# cccl-dailys

A Claude Code plugin by [CCCL](https://cccl.ai) (Claude Code Central London).

Community-built skills for Claude Code users — tips research, resource compilation, and more.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| **cc-tips** | `/cccl-dailys:cc-tips` | Research and compile Claude Code tips & tricks from known experts into a verified, categorized markdown document |

## Installation

### Install from GitHub

```bash
claude plugin install https://github.com/vikrampawar/cccl-dailys
```

### Install from local directory (for development)

```bash
# Clone the repo
git clone https://github.com/vikrampawar/cccl-dailys.git

# Install from local path
claude plugin install ./cccl-dailys
```

### Verify installation

```bash
# List installed plugins
claude plugin list
```

## Usage

### cc-tips — Claude Code Tips & Tricks Researcher

Researches the web for Claude Code tips from Anthropic engineers, official docs, and community experts, then compiles them into a structured markdown file.

```bash
# Generate tips file (default: cc-tips.md in current directory)
/cccl-dailys:cc-tips

# Generate with custom output filename
/cccl-dailys:cc-tips cc-tips-2026-03-20.md
```

**What it does:**
- Searches for tips from Boris Cherny, Tariq, and other Anthropic team members
- Finds popular community tips from Twitter/X, blogs, YouTube, and forums
- Verifies every source link
- Organizes tips into Basic / Intermediate / Advanced categories
- Outputs a single markdown file with 50+ tips, all source-verified

**Output format:** A structured markdown document with:
- Categorized tips (Basic / Intermediate / Advanced)
- Every tip linked to its source
- Code snippets and examples where relevant
- Full source bibliography

## Examples

The `examples/` directory contains sample outputs so you can see what the skills produce before running them.

### [cc-tips-2026-03-20.md](examples/cc-tips-2026-03-20.md)

The first output from `/cc-tips`, generated on 20 March 2026 at the CCCL Tips & Tricks session. Created by running:

```bash
claude --plugin-dir ~/gitper/cccl-dailys
/cccl-dailys:cc-tips cc-tips-2026-03-20.md
```

Claude launched 4 parallel research agents to search for tips from Anthropic engineers, official docs, and community sources, then compiled and verified everything into a single structured document. The whole process took a few minutes and produced 50+ categorized, source-verified tips.

## Plugin Structure

```
cccl-dailys/
├── .claude-plugin/
│   └── plugin.json        # Plugin manifest
├── skills/
│   └── cc-tips/
│       └── SKILL.md       # Tips research skill
├── examples/
│   └── cc-tips-2026-03-20.md  # Sample output
├── README.md
└── LICENSE
```

## Contributing

Want to add a new skill? Create a directory under `skills/` with a `SKILL.md` file.

See the [Claude Code skills documentation](https://docs.anthropic.com/en/docs/claude-code/skills) for the file format.

## Community

- Website: [cccl.ai](https://cccl.ai)
- Meetup: [Claude Code Central London](https://www.meetup.com/claude-code-central-london-meetup-group)
- Luma: [lu.ma/claude.code.central.london](https://lu.ma/claude.code.central.london)

## License

MIT
