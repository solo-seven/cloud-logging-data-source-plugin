# Building the Plugin

In order to build the plugin, you will need to run `yarn install` and `yarn build` with Node v16. The Go code is built with `mage` with the task `buildAll`. This will put all the files in the build directory `dist`. That directory then needs to be copied or linked to your Grafana plugins directory.

# Releasing the Plugin

In order to release the plugin, you will need to update the version in the `package.json` and this version will need to be the tag that the release is created with.

# Testing the Plugin

To test the plugin, you will need to configure and login to Grafana using the upstream OAuth provider that you are using to authenticate with Google Cloud Logging. The person testing this will need to log into Grafana with that user, and then when they create the datasource, it will pass their token in the "Save and Test" stage of creating the datasource.
