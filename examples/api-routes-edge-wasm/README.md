# API routes with WebAssembly at the edge

Next.js ships with [API routes](https://github.com/vercel/next.js#api-routes), which provide an easy solution to build your own `API`. This example shows how to create an API route using WebAssembly in the Edge Runtime.

## Deploy your own

Deploy the example using [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=next-example) or preview live with [StackBlitz](https://stackblitz.com/github/vercel/next.js/tree/canary/examples/api-routes-edge-wasm)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https://github.com/vercel/next.js/tree/canary/examples/api-routes-edge-wasm&project-name=api-routes-edge-wasm&repository-name=api-routes-edge-wasm)

## How to use

Execute [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init), [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/), or [pnpm](https://pnpm.io) to bootstrap the example:

```bash
npx create-next-app --example api-routes-edge-wasm api-routes-edge-wasm-app
# or
yarn create next-app --example api-routes-edge-wasm api-routes-edge-wasm-app
# or
pnpm create next-app --example api-routes-edge-wasm api-routes-edge-wasm-app
```

Deploy it to the cloud with [Vercel](https://vercel.com/new?utm_source=github&utm_medium=readme&utm_campaign=next-example) ([Documentation](https://nextjs.org/docs/deployment)).

## Compiling Rust to WebAssembly

The API Route invokes the Rust function, which is compiled to WebAssembly. To recompile the WebAssembly binary, you'll need the following prerequisites::

1. [Rust](https://www.rust-lang.org/tools/install)
   The API Route for this example is written in Rust and requires the Rust tool chain to build.
2. [`wasm-pack`](https://github.com/rustwasm/wasm-pack)
   `wasm-pack` is a helpful utility that builds, optimizes and packages Rust in to WebAssembly. This example uses it for the build and optimization step (although does not use it for packaging).
3. [Vercel CLI](https://vercel.com/docs/cli)
   The Vercel CLI lets you run this example locally.

To build the WebAssembly:

```bash
(cd wasm && wasm-pack)
```
