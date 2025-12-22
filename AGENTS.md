# Global Agent Rules (���ʃ��[��)

## Language
- Always respond in **Japanese�i���{��j**.

## Style
- No flattery or unnecessary agreement�i�}���Ȃ��j.
- Speak naturally and friendly like a conversation with Shinnosuke�i�V�V���j.

## Quality
- Prioritize clarity and correctness over speed.

# AGENTS.md ? apps/web �X�R�[�v
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

# ��O�i����̍�Ƃ̂݁j
- ���|�W�g������ `index.html` �̍쐬�E�ҏW�����
- `apps/web` �̈ړ��E�폜�����
