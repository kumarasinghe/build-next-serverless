build-HelloWorld:

	# build Next.js project into a serverless function
	npx build-next-serverless

	# move artifacts out of ./dist for deployment by SAM CLI
	mv ./dist/{.,}* "$(ARTIFACTS_DIR)"