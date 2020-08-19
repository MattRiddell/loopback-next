---
lang: en
title: 'Project Layout Reference'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript
sidebar: lb4_sidebar
permalink: /doc/en/lb4/Project-layout-reference.html
---

LoopBack 4 project files and directories are in the _application root
directory_. Within this directory the standard LoopBack 4 project structure has
these sub-directories:

- `src` - Node application scripts and configuration files.
- `public` - Client JavaScript, HTML, and CSS files.
- `definitions` - API and product definition YAML files (**IBM API Connect
  only**).

{% include tip.html content="By LoopBack naming conventions, artifacts such as models are grouped under their sub-directories. Also, with LoopBack artifact generators, they create class names in CamelCase and file names are in snake-case. For example, if you create a model named `MyUserModel` with the model generator, it creates files `my-user.model.ts` under `src/models`. See [Naming Convention](Command-line-interface.md#naming-convention) for more information.
" %}

The following table uses files in the
[`Todo` example](https://github.com/strongloop/loopback-next/tree/master/examples/todo)
as code references.

<table style="font-size: 90%;">
  <thead>
    <tr>
      <th width="200">File or directory</th>
      <th>Description</th>
      <th width="180">How to access in code</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th colspan="3" style="text-align: center; background-color: #bfbfbf;">Top-level application directory</th>
    </tr>
    <tr>
      <td><code>node-modules/</code> directory</td>
      <td>Contains Node packages as specified as dependencies in <code>package.json</code>. Update with <code>npm update</code>.</td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="https://github.com/strongloop/loopback-next/blob/master/examples/todo/package.json"><code>package.json</code></a></td>
      <td>
        Standard npm package specification. Use it to set up package dependencies, among other things. This file must be in the application root directory. See <a href="https://docs.npmjs.com/files/package.json"><code>npm-package.json</code> for information.</a>.
      </td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><code>README.md</code></a></td>
      <td>Stub file for internal documentation.</td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="https://github.com/strongloop/loopback-next/blob/master/examples/todo/tsconfig.json"><code>tsconfig.json</code></a></td>
      <td>
        A file specifies the root files and the compiler options required to compile the project. See <a href="https://www.typescriptlang.org/docs/handbook/tsconfig-json.html"><code>tsconfig.json</code> for information.</a>.
      </td>
      <td>N/A</td>
    </tr>
    <tr>
      <th colspan="3" style="text-align: center; background-color: #bfbfbf;">/src directory - Node application files</th>
    </tr>
    <tr>
      <td><code>controllers/</code> directory</td>
      <td>A sub-directory for all controller files. See <a href="Controller.html">Controller</a>.</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><code>datasources/</code> directory</td>
      <td>A sub-directory for all dataSource files. See <a href="DataSource.html">DataSource</a>.</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><code>models/</code> directory</td>
      <td>A sub-directory for all model files. See <a href="Model.html">Model</a>.</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><code>repositories/</code> directory</td>
      <td>A sub-directory for all repository files. See <a href="Repository.html">Repository</a>.</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><a href="https://github.com/strongloop/loopback-next/blob/master/examples/todo/src/application.ts"><code>application.ts</code></a></td>
      <td>Main application program file. A central registry file for inversion of control and dependency injection. See <a href="Application.html">Application</a>.</td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="https://github.com/strongloop/loopback-next/blob/master/examples/todo/src/index.ts"><code>index.ts</code></a></td>
      <td>A script that initializes and runs the application.</td>
      <td>N/A</td>
    </tr>
    <tr>
      <td><a href="https://github.com/strongloop/loopback-next/blob/master/examples/todo/src/migrate.ts"><code>migrate.ts</code></a></td>
      <td>A script to run database migration. See <a href="Database-migrations.html">Database Migrations</a>.</td>
      <td><code>npm run build && npm run migrate</code></td>
    </tr>
    <tr>
      <td><a href="https://github.com/strongloop/loopback-next/blob/master/examples/todo/src/openapi-spec.ts"><code>openapi-spec.ts</code></a></td>
      <td>A script that exports the OpenAPI spec from the application.</td>
      <td><code>npm run build && npm run openapi-spec</code></td>
    </tr>
    <tr>
      <td><a href="https://github.com/strongloop/loopback-next/blob/master/examples/todo/src/sequence.ts"><code>sequence.ts</code></a></td>
      <td>A file where to define a series of steps to control how a specific type of `Server`
      responds to incoming requests. See <a href="Sequence.html">Sequence</a>.</td>
      <td>N/A</td>
    </tr>
    <tr>
      <th colspan="3" style="text-align: center; background-color: #bfbfbf;">/public directory - Client application files</th>
    </tr>
    <tr>
      <td><a href="https://github.com/strongloop/loopback-next/blob/master/examples/todo/public/index.html"><code>index.html</code></a></td>
      <td>An example LoopBack front page.</td>
      <td>N/A</td>
    </tr>
    <tr>
      <td>Others</td>
      <td>Add your HTML, CSS, client JavaScript files.</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>
