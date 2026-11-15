# HomeLang-CompilerDesign

A compiler for **HomeLang**, a small smart-home automation language
(`IF TEMPERATURE > 30 THEN TURN_ON AC`), built as a Compiler Design project.
It takes a program from source text to a simulated home, one stage at a time.

## Pipeline

```
Source -> Lexer -> Parser -> Semantic analysis -> IR + Optimizer -> Codegen + Runtime
```

Each stage is a pure function that hands its result to the next. A stage with
errors stops the pipeline; warnings do not.

## Team and ownership

| # | Stage | Owner | Folder |
|---|-------|-------|--------|
| 1 | Lexer, project scaffold, UI shell | _TBD_ | `src/compiler/lexer/`, `src/ui/` |
| 2 | Parser | _TBD_ | `src/compiler/parser/` |
| 3 | Semantic analysis | _TBD_ | `src/compiler/semantic/` |
| 4 | IR and optimizer | _TBD_ | `src/compiler/ir/`, `src/compiler/opt/` |
| 5 | Codegen, runtime and simulator | _TBD_ | `src/compiler/codegen/`, `src/compiler/runtime/` |

Each owner adds a short section below about their stage once it is merged.

## Getting started

```sh
npm install
npm run dev        # start the visual walkthrough
npm test           # unit, golden and differential tests
npm run build      # type-check and build
```

See [CONTRIBUTING.md](CONTRIBUTING.md) for the branch, review and merge rules.
