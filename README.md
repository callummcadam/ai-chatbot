<a href="https://chat.vercel.ai/">
  <img alt="Next.js 14 and App Router-ready AI chatbot." src="https://chat.vercel.ai/opengraph-image.png">
  <h1 align="center">Next.js AI Chatbot</h1>
</a>

<p align="center">
  An open-source AI chatbot app template built with Next.js, the Vercel AI SDK, OpenAI, and MongoDB.
</p>

<p align="center">
  <a href="#features"><strong>Features</strong></a> ·
  <a href="#model-providers"><strong>Model Providers</strong></a> ·
  <a href="#deploy-your-own"><strong>Deploy Your Own</strong></a> ·
  <a href="#running-locally"><strong>Running locally</strong></a> ·
  <a href="#authors"><strong>Authors</strong></a>
</p>
<br/>

## Features

- [Next.js](https://nextjs.org) App Router
- React Server Components (RSCs), Suspense, and Server Actions
- [Vercel AI SDK](https://sdk.vercel.ai/docs) for streaming chat UI
- Support for OpenAI (default), Anthropic, Cohere, Hugging Face, or custom AI chat models and/or LangChain
- [shadcn/ui](https://ui.shadcn.com)
  - Styling with [Tailwind CSS](https://tailwindcss.com)
  - [Radix UI](https://radix-ui.com) for headless component primitives
  - Icons from [Phosphor Icons](https://phosphoricons.com)
- Chat History, rate limiting, and session storage with [MongoDB](https://www.mongodb.com)
- [NextAuth.js](https://github.com/nextauthjs/next-auth) for authentication (GitHub, Google)
- Support for email pattern matching to restrict access to a specific email domain

## Model Providers

This template ships with OpenAI `gpt-3.5-turbo` as the default. However, thanks to the [Vercel AI SDK](https://sdk.vercel.ai/docs), you can switch LLM providers to [Anthropic](https://anthropic.com), [Cohere](https://cohere.com/), [Hugging Face](https://huggingface.co), or using [LangChain](https://js.langchain.com) with just a few lines of code.

## Deploy Your Own

You can deploy your own version of the Next.js AI Chatbot to Vercel with one click:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?demo-title=Next.js%2BChat&demo-description=A%2Bfull-featured%2C%2Bhackable%2BNext.js%2BAI%2Bchatbot%2Bbuilt%2Bby%2BVercel%2BLabs&demo-url=https%3A%2F%2Fchat.vercel.ai%2F&demo-image=%2F%2Fimages.ctfassets.net%2Fe5382hct74si%2F4aVPvWuTmBvzM5cEdRdqeW%2F4234f9baf160f68ffb385a43c3527645%2FCleanShot_2023-06-16_at_17.09.21.png&project-name=Next.js%2BChat&repository-name=nextjs-chat&repository-url=https%3A%2F%2Fgithub.com%2FQuantumSlipstream%2Fai-chatbot&from=templates&skippable-integrations=1&env=OPENAI_API_KEY%2CAUTH_SSO_ENABLED%2CAUTH_SECRET%2CAUTH_GITHUB_ENABLED%2CAUTH_GITHUB_ID%2CAUTH_GITHUB_SECRET%2CAUTH_GOOGLE_ENABLED%2CAUTH_GOOGLE_ID%2CAUTH_GOOGLE_SECRET%2CMONGODB_URI&envDescription=How%2Bto%2Bget%2Bthese%2Benv%2Bvars&envLink=https%3A%2F%2Fgithub.com%2FQuantumSlipstream%2Fai-chatbot%2Fblob%2Fmain%2F.env.example&teamCreateStatus=hidden)

## Creating a MongoDB Database Instance

Please adhere to the instructions provided in the [quick start guide](https://docs.mongodb.com/guides/server/drivers/#getting-driver) offered by MongoDB. This guide will walk you through the process of setting up and configuring your MongoDB database instance, allowing your application to seamlessly communicate with it.

Remember to update your environment variables (`MONGODB_URI`) within the `.env` file with the correct credentials furnished during the MongoDB database setup.

Note: It's crucial to ensure the security of your MongoDB instance. If your IP address is not whitelisted, you will be unable to connect to the database, and incoming messages will not be saved. Depending on your specific use case, consider whitelisting the IP address of your cloud hosting provider within the MongoDB security settings. Alternatively, if you have a dynamic IP address, it is advisable to whitelist all IPs using the range 0.0.0.0/0 to ensure uninterrupted access.

## Running locally

You will need to use the environment variables [defined in `.env.example`](.env.example) to run Next.js AI Chatbot. It's recommended you use [Vercel Environment Variables](https://vercel.com/docs/projects/environment-variables) for this, but a `.env` file is all that is necessary.

> Note: You should not commit your `.env` file or it will expose secrets that will allow others to control access to your various OpenAI and authentication provider accounts.

1. Install Vercel CLI: `npm i -g vercel`
2. Link local instance with Vercel and GitHub accounts (creates `.vercel` directory): `vercel link`
3. Download your environment variables: `vercel env pull`

```bash
pnpm install
pnpm dev
```

Your app template should now be running on [localhost:3000](http://localhost:3000/).

## Authors

This project is created by [Vercel](https://vercel.com) and [Next.js](https://nextjs.org) team members, with contributions from:

- Jared Palmer ([@jaredpalmer](https://twitter.com/jaredpalmer)) - [Vercel](https://vercel.com)
- Shu Ding ([@shuding\_](https://twitter.com/shuding_)) - [Vercel](https://vercel.com)
- shadcn ([@shadcn](https://twitter.com/shadcn)) - [Vercel](https://vercel.com)
