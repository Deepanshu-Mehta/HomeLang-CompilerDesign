# Contributing

Five people each own one compiler stage (see the table in the README).

## Workflow

1. Never push to `main`. Create a branch named `feat/<stage>`, for example `feat/lexer`.
2. Make several small commits under your own account. A good order is
   source, then tests, then the UI card, then docs.
3. Open a pull request and get one review before merging.
4. Review the next person's pull request: 1 -> 2 -> 3 -> 4 -> 5 -> 1.

## Merge order

Stages depend on the previous one, so merge in this order:
lexer, parser, semantic, IR and optimizer, codegen and runtime.
The shared interface files (tokens, AST, quads, bytecode, semantic types) are
already in `main`, so everyone can start at the same time.

## Rules

- Stay inside your own folders. Changing a shared interface file needs a
  heads-up to every owner whose stage uses it.
- Run `npm test` and `npm run build` before opening a pull request.
- Write a commit message that says what changed and why.
