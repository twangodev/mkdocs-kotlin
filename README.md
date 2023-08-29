# mkdocs-kotlin-playground
Replaces fenced code blocks with the language `kotlin` with an interactive Kotlin Playground.

## Usage
First, copy `kotlin.js` and `kotlin.css` into the respective `javascripts` and `stylesheets` directories in your mkdocs project.

Next add the following to your `mkdocs.yml`:
```yaml
extra_javascript:
  - javascripts/kotlin.js
  - https://unpkg.com/kotlin-playground@1
  
extra_css:
    - stylesheets/kotlin.css
```

This plugin activates the Kotlin Playground for all fenced code blocks with the language `kotlin`.

## Extra Features

### Kotlin Playground Options
#### `//sampleStart` and `//sampleEnd`
You can use `//sampleStart` and `//sampleEnd` to specify a range of lines to be shown in the Kotlin Playground. This is useful if you want to show a small snippet of code in the documentation, but want to allow users to edit the entire file.

For example, to show the contents of the `main` function in the Kotlin Playground:
```kotlin
fun myHiddenFunction() {
    println("mystery")
}

fun main() {
//sampleStart
    println("Hello World!")
    myHiddenFunction()
//sampleEnd
}
```