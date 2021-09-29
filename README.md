# hhvm-user-documentation-graph

The Abstract Syntax tree of https://github.com/hhvm/user-documentation in ArangoDB.

![Preview of the ArangoDB editor](https://i.imgur.com/47hoBTJ.png)

## Restoring the dataset

1. Install the CLI tools

```bash
$ brew install arangodb
```

Or download the CLI tools from https://www.arangodb.com/download-major/macosx/

2. Start a docker instance

```bash
$ docker run -e ARANGO_NO_AUTH=1 -p 8529:8529 arangodb
```

3. Confirm the database is working

Go to http://localhost:8529 and confirm you can see the UI

4. Restore the backup

Run the following command from the project root to restore the dataset:
```bash
arangorestore --input-directory dump --server.authentication=false --include-system-collections true
```

5. Done!

