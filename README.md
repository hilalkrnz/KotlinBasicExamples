# KotlinBasicExamples
Bu repository Udemy' den aldığım Kasım Adalan' ın kotlin kursunda bize verdiği ödevleri göstermek için oluşturdum.

<details><summary>Ödev1</summary>
<p>

 -> Kullanıcıdan alınan sıcaklık değerini Fahrenhiet' a dönüştüren metod yazınız.
  
  ```
  class Fahrenhiet {

    fun convert(temprature : Double): Double{
        val result = temprature * (1.8) + 32

        return result
    }
}
```

```
fun main(){

    val e1 = Fahrenhiet()

    val input = Scanner(System.`in`)

    println("Sıcaklığı giriniz : ")

    val temprature = input.nextDouble()

    val result = e1.convert(temprature)

    println("Fahrenhiet Dönüşümü :  $result")

}
```

**Çıktı**
```
Sıcaklığı giriniz : 
32
Fahrenhiet Dönüşümü :  89.6

```
</p>
</details>

<details><summary>Ödev2</summary>
<p>

 -> Dikdörtgen çevresini hesaplayan metodu yazınız.
 
 ```
 class Rectangle {

    fun calculate (longSide : Int, shortSide : Int) : Int {

        val result = 2 * (longSide + shortSide)

        return result;
    }
}
 ```
 
 ```
 fun main(){

    val e2 = Rectangle()

    val input = Scanner(System.`in`)

    println("Büyük kenarı giriniz : ")

    val longSide = input.nextInt()

    println("Küçük kenarı giriniz : ")

    val shortSide = input.nextInt()

    val result = e2.calculate(longSide, shortSide)

    println("Dikdörtgenin çevresi :  $result")

}
 ```
 
 **Çıktı**
 ```
 Büyük kenarı giriniz : 
35
Küçük kenarı giriniz : 
20
Dikdörtgenin çevresi :  110

 ```
 </p>
</details>

<details><summary>Ödev3</summary>
<p>

-> Sayının fatöriyel değerini hesaplayıp geri döndüren metodu yazınız.
```
fun main(){

    fun factorial(num : Int) : Int{
        var result = 1
        for (i in 1..num){
          result = result * i
        }
        return result
    }

    val input = Scanner(System.`in`)

    println("Sayıyı giriniz : ")

    val num = input.nextInt()

    val result = factorial(num)

    println("$num' nın faktöriyeli : $result")
}
```

**Çıktı**
```
Sayıyı giriniz : 
6
6' nın faktöriyeli : 720

```
</p>
</details>

<details><summary>Ödev4</summary>
<p>

-> Sayının fatöriyel değerini hesaplayıp geri döndüren metodu yazınız.
```
