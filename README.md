# Templates-in-nested-addons

This is a repo to demonstrate the issue of using an addon (ember-cli-htmlbars) that adds a preprocessor inside of another addon (the in-repo addon named `has-templates-in-addon-tree`).

Under 0.1.15 the following error is thrown:

```javascript
Missing template processor
Error: Missing template processor
    at module.exports.preprocessTemplates (/Users/rjackson/Source/sandbox/ember-cli/templates-in-nested-addons/node_modules/ember-cli/lib/preprocessors.js:83:11)
    at EmberApp._processedTemplatesTree (/Users/rjackson/Source/sandbox/ember-cli/templates-in-nested-addons/node_modules/ember-cli/lib/broccoli/ember-app.js:523:10)
    at EmberApp.appAndDependencies (/Users/rjackson/Source/sandbox/ember-cli/templates-in-nested-addons/node_modules/ember-cli/lib/broccoli/ember-app.js:754:24)
    at EmberApp.javascript (/Users/rjackson/Source/sandbox/ember-cli/templates-in-nested-addons/node_modules/ember-cli/lib/broccoli/ember-app.js:814:34)
    at EmberApp.toArray (/Users/rjackson/Source/sandbox/ember-cli/templates-in-nested-addons/node_modules/ember-cli/lib/broccoli/ember-app.js:1115:10)
    at EmberApp.toTree (/Users/rjackson/Source/sandbox/ember-cli/templates-in-nested-addons/node_modules/ember-cli/lib/broccoli/ember-app.js:1137:30)
    at Object.<anonymous> (/Users/rjackson/Source/sandbox/ember-cli/templates-in-nested-addons/Brocfile.js:24:22)
    at Module._compile (module.js:456:26)
    at Object.Module._extensions..js (module.js:474:10)
    at Module.load (module.js:356:32)
```
