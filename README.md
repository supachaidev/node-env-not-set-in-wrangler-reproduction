# NODE_ENV Not Set in Wrangler Process

## Expected Behavior

After we set `NODE_ENV` in the `wrangler dev` command such as `NODE_ENV=development wrangler dev`, the `process.env.NODE_ENV` in the `src/index.ts` should be evaluated to `"development"`.

## Current Behavior

`process.env.NODE_ENV` is always evaluated to `"production"` no matter what value we set `NODE_ENV` to in the `wrangler dev` command.

## Steps to Reproduce

1. Clone the project.
2. Run `pnpm install`.
3. Run `pnpm start`. There will be the `NODE_ENV: production` (which should be `NODE_ENV: development`) in the Terminal console.
