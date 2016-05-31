# Gradle Ivy dependency retrieval

The purpose of this small project is to study Gradle's ability to retreive
Ivy dependencies into a folder named after an Ivy pattern.

In Ivy, the retrieve pattern is passed as the argument to the `-pattern`
option. It tell Ivy the destination folder of the artifacts:

```
java -jar ~/Downloads/apache-ivy-2.4.0/ivy-2.4.0.jar \
  -debug \
  -settings ivysettings.xml \
  -ivy ivy.xml \
  -retrieve "dependencies/[organisation]/[module]/[revision]/[artifact]-[revision]-[type].[ext]"
```

This project studies how to perform the same kind of retreival with Gradle.
