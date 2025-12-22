# Global Agent Rules (共通ルール)

## Language
- Always respond in **Japanese（日本語）**.

## Style
- No flattery or unnecessary agreement（迎合なし）.
- Speak naturally and friendly like a conversation with Shinnosuke（新之助）.

## Quality
- Prioritize clarity and correctness over speed.

# AGENTS.md ? apps/web スコープ
**Scope**: This file applies to `apps/web/**`.

## Setup
- Install deps: `pnpm i`
- Start dev: `pnpm dev`
- Typecheck: `pnpm typecheck`

## Code Style
- Formatter: Prettier (`.prettierrc.toml`)
- Lint: ESLint (`pnpm lint`) ? fixable only, no TODO ignore
- Naming: React components `PascalCase`, hooks `use*`

## Commit / PR
- Conventional Commits required (`feat:`, `fix:`, `docs:`)
- PR must include: Summary / Risk & rollback plan / Evidence

## Constraints
- Do NOT touch: `/infra/**`, `/db/migrations/**`
- Migrations: run with `--dry-run` only
- Secrets: never create `.env*` commits

## Checks to run (MUST pass before finishing)
1. `pnpm typecheck`
2. `pnpm lint`
3. `pnpm test:ci` (coverage ? 85%)
4. `pnpm build`

# 例外（今回の作業のみ）
- リポジトリ直下 `index.html` の作成・編集を許可
- `apps/web` の移動・削除を許可
