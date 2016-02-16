# Find duplicate code with jscpd (2016-02-16)
[jscpd](https://github.com/kucherenko/jscpd) is a great tool for finding duplicate pieces of JavaScript (and not only) code. A sample config looks like:
```yaml
exclude:
  - "**/node_modules/**"
files:
  - "**/*.js"
min-lines: 8
min-tokens: 80
output: "cpd.xml"
```

Now running just `jscpd` will generate `cpd.xml`. It's in the [CPD](http://pmd.sourceforge.net/pmd-4.3.0/cpd.html) format, which makes it a great fit for the [DRY plugin](https://wiki.jenkins-ci.org/display/JENKINS/DRY+Plugin) in Jenkins.
