The manifest holds metadata used by the `auv-repo` tool to manage multiple git repositories as part of the larger project as a whole.

`manifest.json` in this repo holds the details about all of the different projects.
```
{
  "fetch": "git@github.com:uscauv/" <= this is the prefix to all of the project's remote URLs
  "projects": [
    {
      "name": name of the project on GitHub (this will be appended to "fetch" when cloning)
      "path": path where the project is cloned to. this can be useful for further organization as related projects can be organized further under a subdirectory
      "branch": git branch to clone from (this is optional and will default to "master" if ommitted)
    }
  ]
}
```

When a new repository is created, it must be added to the manifest so other clients will pull it down automatically.
