# Basic-Codelab
### ■screen shot
![Untitled](https://user-images.githubusercontent.com/129733584/233834048-0bc73855-f01d-427a-9a93-23f315e48a10.gif)

### ■reference

- [Jetpack Compose basics](https://developer.android.com/codelabs/jetpack-compose-basics#0)
- [List of Compose Modifiers](https://developer.android.com/jetpack/compose/modifiers-list)
    - [Use function types and lambda expressions in Kotlin](https://developer.android.com/codelabs/basic-android-kotlin-compose-function-types-and-lambda#2)
- [Animation Doc](https://developer.android.com/jetpack/compose/animation)
- Icons dependencies <br>
  `implementation "androidx.compose.material:material-icons-extended:$compose_version"`

### ■partical kotlin training 

```
// Use function types and lambda expressions in Kotlin
import kotlinx.coroutines.*


fun main() {
    val treatFunction = trickOrTreat(isTrick = false){ "Have $it quarters!" }
    val trickFunction = trickOrTreat(isTrick = true, extraTreat = null)
    treatFunction()
    repeat(4) {
    	trickFunction()
    }
}

val trick = {
    println("No treats!")
}
val treat: () -> Unit = {
    println("Have a treat!")
}

fun trickOrTreat(isTrick: Boolean, extraTreat: ((Int) -> String)? ): () -> Unit {
    if(isTrick) {
        return trick
    } else {
        if(extraTreat != null) {
        	println(extraTreat(5))
        }
        return treat
    }
}
```
