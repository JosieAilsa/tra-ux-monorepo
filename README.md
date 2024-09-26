# Tom Allen UX 

- A rebuild of square space portfolio - except it doesn't cost £15 a month!
- Using this to learn Nuxt and TypeScript in the process 😅
- Built from using [Nuxt](https://nuxt.com/) for the front end and [Sanity](https://www.sanity.io/) to handle its content, from a template developed by the sanity team.

## Getting started

Run the following commands to prepare both applications, each step should be executed from the **root directory**:

1. Install dependencies.

```sh
pnpm install
```

2. Select or create a Sanity project and dataset, and output the details to a `.env` file.

```sh
cd studio && pnpm sanity init --env .env
```

3. [Generate a token](https://www.sanity.io/docs/http-auth#4c21d7b829fe) with read permissions for use in the next step.

```sh
pnpm sanity manage
```

4. Copy the example app `.env` file and populate it with the required values.

```sh
cp ./app/.env.example ./app/.env
```

5.  Start the development servers:

```sh
pnpm dev
```
