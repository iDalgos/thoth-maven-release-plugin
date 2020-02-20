# thoth-maven-release-plugin

I created this project to research how the maven-release-plugin automatically increments version numbers. 
The POM configuration allows the maven-release-plugin to run "locally" without making any tags on your
production source control system.

I needed to do this research because I wanted to change the format of my version numbers to include
a qualifier. Version numbers are typically formatted as "1.0.0.0-SNAPSHOT". If this format is changed to include
a qualifier (1.0.0.0-qualifier-SNAPSHOT), how would the maven-release-plugin react? Would it increment the 
number as expected? Will it do something weird? Does it matter if you use a "-" or a "." to separate words? 

This project allowed me to answer these questions. The version number should follow this format:

```txt
1.0.0.0-some-cool-qualifier-SNAPSHOT
```

The numbers are separated by the "." character. The "-" character is used to separate the numbers from
the qualifier. Individual words of the qualifier are separated by the "-" character. Finally end in "-SNAPSHOT".