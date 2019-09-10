# Swagger-pet

NPM version Build Status Code Climate Dependency Status devDependency Status Build Status

🕰️ Looking for the older version of Swagger Editor? Refer to the 2.x branch.

Swagger Editor lets you edit Swagger API specifications in YAML inside your browser and to preview documentations in real time. Valid Swagger JSON descriptions can then be generated and used with the full Swagger tooling (code generation, documentation, etc).

As a brand new version, written from the ground up, there are some known issues and unimplemented features. Check out the Known Issues section for more details.

This repository publishes to two different NPM modules:

swagger-editor is a traditional npm module intended for use in single-page applications that are capable of resolving dependencies (via Webpack, Browserify, etc).
swagger-editor-dist is a dependency-free module that includes everything you need to serve Swagger Editor in a server-side project, or a web project that can't resolve npm module dependencies.
If you're building a single-page application, using swagger-editor is strongly recommended, since swagger-editor-dist is significantly larger.

For the older version of swagger-editor, refer to the 2.x branch.

Running locally
Prerequisites
Node 6.x
NPM 3.x
If you have Node.js and npm installed, you can run npm start to spin up a static server.

Otherwise, you can open index.html directly from your filesystem in your browser.

If you'd like to make code changes to Swagger Editor, you can start up a Webpack hot-reloading dev server via npm run dev.

Browser support
Swagger Editor works in the latest versions of Chrome, Safari, Firefox, Edge and IE11.

Known Issues
To help with the migration, here are the currently known issues with 3.X. This list will update regularly, and will not include features that were not implemented in previous versions.

Everything listed in Swagger UI's Known Issues.
The integration with the codegen is still missing.
Importing specs from a URL is not implemented.
Docker
Running the image from DockerHub
There is a docker image published in DockerHub.

To use this, run the following:

docker pull swaggerapi/swagger-editor
docker run -d -p 80:8080 swaggerapi/swagger-editor
This will run Swagger Editor (in detached mode) on port 80 on your machine, so you can open it by navigating to http://localhost in your browser.

Building and running an image locally
To build and run a docker image with the code checked out on your machine, run the following from the root directory of the project:

# Install npm packages (if needed)
npm install

# Build the app
npm run build

# Build an image
docker build -t swagger-editor .

# Run the container
docker run -d -p 80:8080 swagger-editor

You can then view the app by navigating to http://localhost in your browser.

Documentation
Importing your OpenAPI document
Security contact
Please disclose any security-related issues or vulnerabilities by emailing security@swagger.io, instead of using the public issue tracker.

License
Copyright 2018 SmartBear Software

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
