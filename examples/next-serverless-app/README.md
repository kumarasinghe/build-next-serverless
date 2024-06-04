# Next Serverless Example

This example intends to [show you the changes needed to add serverless support](https://github.com/kumarasinghe/build-next-serverless/commit/96bba523ad3b58ff5fae516077a7b8919f89d8f8) to your own Next.js app.<br/>
It contains a HelloWorld Serverless function which uses `build-next-serverless` for building and `AWS SAM CLI` for deployment.

## Building & Deploying

1. [Setup AWS SAM CLI.](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-getting-started.html)

2. Build the function:

   ```sh
   cd my-next-app
   sam build HelloWorld --build-in-source --use-container
   ```

   This command will execute the `Makefile` behind the scene, which will hand over the build process to `build-next-serverless`

3. Test locally:

   ```sh
   sam local invoke HelloWorld
   ```

   Your lambda will be invoked inside a Docker container.

4. Deploy

   ```sh
   sam deploy --guided
   ```

   HelloWorld function will be deployed according to the infrastructure specified in `template.yaml`<br/>
   `--guided` switch will be only needed for your first deployment.
