# Serverless Stack Termination Protection Plugin

Following deployment, the Serverless Framework does not have the option to enable termination protection for the CloudFormation stack. This plugins will enable the termination protection. It can also disable it by using a command line option. This plugin is designed for the Serverless Framework 1.x.

## Requirements

- Serverless Framework 1.x.
- Node 8.x or greater.

## Installation

Install with **npm**:

```sh
npm install --save-dev serverless-stack-termination-protection
```

And then add the plugin to your `serverless.yml` file:

```yaml
plugins:
  - serverless-stack-termination-protection
```

## Using the Plugin

### Automatically Enable Termination Protection After Deployment

This plugin enables termination protection automatically after the deployment. Simply run the **deploy**:

```sh
sls deploy
```

### Automatically Disable Termination Protection After Deployment

This plugin can disable termination protection automatically after the deployment. Simply run the **deploy** with the **--disable-termination-protection** option:

```sh
sls deploy --disable-termination-protection
```

### Notes

This verion is not designed to work with a custom stack name defined in the `serverless.yml` file:

```yaml
provider:
  stackName: custom-stack-name
```

## License

See the included [LICENSE](LICENSE) for rights and limitations under the terms of the MIT license.
