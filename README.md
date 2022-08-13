# Greatest Common Divisor Calculator - Spotbugs

For this exercise, we'll add the Spotbugs plugin to our reporting output to help us find errors in our program.

[Spotbugs](https://spotbugs.github.io/) can help you find potential bugs on your Java programs by using static analysis
to detect code instances that are likely to be errors.

One option to use it is through its maven plugin. We'll use it in that way for this exercise.

The attached code includes an extra class containing errors that are 
commonly picked up by spotbugs.

1. We added a reporting section to the `pom.xml`, within this section add the spotbugs plugin. Similar to the code below.

```
<reporting>
    <plugins>
        <plugin>
            <groupId>com.github.spotbugs</groupId>
            <artifactId>spotbugs-maven-plugin</artifactId>
            <version>4.1.4</version>
        </plugin>
    </plugins>
</reporting>
```

2. We ran `mvn compile site`.

3. You can check the generated report on `target/site/spotbugs.html`. What error patterns does it show?

4. Optional, you can check what other errors can be detected by spotbugs on [their site](https://spotbugs.readthedocs.io/en/latest/bugDescriptions.html).