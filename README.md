# figma-tokens & Style dictionary pipeline.

This repository transforms your tokens stored on Figma Tokens (with GitHub sync enabled) to be automatically transformed with token-transformer and Style Dictionary in a multi-theme environment.

Change your tokens in `tokens.json` (either directly or with the Figma Tokens plugin in Figma). The GitHub action will automatically generate tokens to the `tokens/` directory that can then be read by Style Dictionary, which will output tokens to the format you defined in `build.js` - css variables will be generated in the `output` directory.

## Token implemementation

Tokens are delivered through JSDeliver. Each theme is a separate file, and the tokens are defined in the `{theme}.css` file.

For the tokens to become available through the CDN, you need to publish a new version of the tokens in Github.

Tokens can be accessed based on their version by using `@0.0.1` or by `@latest` to access the latest version.

- Light theme: https://cdn.jsdelivr.net/gh/brandcodeapp/bc-design-tokens@latest/output/light.css
- Dark theme: https://cdn.jsdelivr.net/gh/brandcodeapp/bc-design-tokens@latest/output/dark.css
