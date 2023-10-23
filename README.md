## prereqs

```bash
pnpm install
```

## with `"sideEffects": false`

```bash
pnpm build
grep -R 'example-job' .next

# no match
```

## with `"sideEffects": ["./jobs/**/*.ts"]`

```bash
pnpm build
grep -R 'example-job' .next

# .next/server/app/api/trigger/route.js matches
```