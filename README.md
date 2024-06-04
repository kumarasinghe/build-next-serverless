# Build Next.js for Serverless

Build your Next.js projects for deployment in serverless environments such as AWS Lambda.

✔️ No installation required<br/>
✔️ Minimal base package size (~25mb with Next 14)<br/>
✔️ Test your build in server mode<br/>

### Build

1. Enable _standalone mode_ in your `next.config.mjs`:

   ```diff
   ...
   const nextConfig = {
   +    output: "standalone",
   };
   ...
   ```

2. Run the build command in your project folder:

   ```sh
   cd my-next-app
   npx build-next-serverless
   ```

The serverless function will be built into `dist` directory.<br/>
You can test the build using the server mode with: `node dist/server.js`

> ### Important!
>
> You should build your functions in a serverless alike environment.<br/>
> This ensures your `node_modules` are compatible with the target serverless runtime.<br/>
> To achieve that, we recommend you to use a deployment tool like `AWS SAM CLI`

There is an [an example](https://github.com/kumarasinghe/build-next-serverless/tree/develop/examples/next-serverless-app) showing how to incorporate `AWS SAM CLI` into your workflow.
