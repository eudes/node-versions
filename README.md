node-versions
=============

Outputs current versions of installed packages. By douyw, extracted from http://stackoverflow.com/a/13381344 (visit for complete info)

usage
=====

To create a packages.json with currently installed versions:

0. download versions.js and put it in the root of your package
1. `npm init` and follow instructions at will to generate a basic packages.json
2. `node versions.js`
3. copy the output and paste it in the `"dependencies"` block of your packages.json
4. don't forget to erase the last comma in the list of dependencies

example
=======

`npm init` creates a package.json like this:
```
{
  "name": "test.js",
  "version": "1.0.0",
  
  ...
  
  "dependencies": {
    "colors": "*",
    "commander": "*",
    "htmlparser": "*",
    "optimist": "*",
    "progress": "*",
    "request": "*",
    "soupselect": "*"
  }
}
```

`node versions.js` outputs:

```
"colors": "0.6.0-1",
"commander": "1.0.5",
"htmlparser": "1.7.6",
"optimist": "0.3.5",
"progress": "0.1.0",
"request": "2.11.4",
"soupselect": "0.2.0",   // Remember: remove the comma character in the last line.
```

Final package.json should look like this:

```
{
  "name": "test.js",
  "version": "1.0.0",
  
  ...
  
  "dependencies": {
    "colors": "0.6.0-1",
    "commander": "1.0.5",
    "htmlparser": "1.7.6",
    "optimist": "0.3.5",
    "progress": "0.1.0",
    "request": "2.11.4",
    "soupselect": "0.2.0"
  }
}
```
