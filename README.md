# KotlinBasicExamples
Bu repository de Udemy' den aldığım Kasım Adalan' ın kotlin kursunda verilmiş olan ödevleri çözümlerimle göstermek istedim.
```
* Fahrenheit Dönüştürme
* Dikdörtgen Çevre Hesaplama
* Faktöriyel Hesaplama
* Kelimede Harf Sayısı Bulma
* Maaş Hesabı
* İnternet Kota Hesabı
```
<details><summary>Ödev1</summary>
<p>

 -> Kullanıcıdan alınan sıcaklık değerini Fahrenheit' a dönüştüren metod yazınız.
  
  ```
  class Fahrenheit {

    fun convert(temprature : Double): Double{
        val result = temprature * (1.8) + 32

        return result
    }
}
```

```
fun main(){

    val e1 = Fahrenheit()

    val input = Scanner(System.`in`)

    println("Sıcaklığı giriniz : ")

    val temprature = input.nextDouble()

    val result = e1.convert(temprature)

    println("Fahrenheit Dönüşümü :  $result")

}
```

**Çıktı**
```
Sıcaklığı giriniz : 
32
Fahrenheit Dönüşümü :  89.6
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

-> Sayının faktöriyel değerini hesaplayıp geri döndüren metodu yazınız.
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

-> Girilen kelimede belirtilen harfin kaç defa tekrar ettiğini döndüren metod yazınız.

```
class Letters {

    fun findLetters(word : String, letter : Char) : Int{

        var counter = 0
        for(i in word){
            if (i == letter){
                counter++
            }

        }
        return counter
    }
}
```

```
fun main(){

    val e4 = Letters()

    val input = Scanner(System.`in`)

    println("Kelimeyi giriniz : ")

    val word = input.next()

    println("Harfi giriniz : ")

    val letter = input.next()[0]

    val result = e4.findLetters(word, letter)

    println("$letter harfi $result defa kullanılmıştır.")
}
```
**Çıktı**

```
Kelimeyi giriniz : 
papatya
Harfi giriniz : 
p
p harfi 2 defa kullanılmıştır.
```

</p>
</details>

<details><summary>Ödev5</summary>
<p>

-> Girilen gün sayısına göre maaş hesabı yapan ve elde edilen değeri geri döndüren metodu yazınız.
               
                     1 günde sekiz saat çalışılabilir.
                     Çalışma saati ücreti : 10 TL 
                     Mesai saati ücreti : 20 TL
                     160 saat üzeri mesai sayılır.
                     
 ```                    
class DailySalary {

    fun salaryCalculation(day : Int): Int {

        var hours = day * 8

        var salary = 0

        if (hours < 160){

            salary = hours * 10

        }else{

            salary = (hours - 160) * 20 + 160 * 10
        }

        return salary
    }
}
```

```
fun main(){

    val e5 = DailySalary()

    val input = Scanner(System.`in`)

    println("Kaç gün çalıştınız ? ")

    val day = input.nextInt()

    val result = e5.salaryCalculation(day)

    println("Maaşınız $result tl' dir.")
}
```

**Çıktı**
```
Kaç gün çalıştınız ? 
40
Maaşınız 4800 tl' dir.
```

</p>
</details>

<details><summary>Ödev6</summary>
<p>

-> Girilen kota miktarına göre ücreti hesaplayarak geri döndüren metodu yazınız.               
                    
                     50GB 100 TL 
                     Kota aşımından sonra her 1GB 4 TL

```
class InternetQuota {

    fun quotaCalculation(quota: Int) : Int{

        var payment = 0

        if (quota < 50){
            print("Hatalı kota girdiniz.")
        }else if (quota == 50){
            payment = 100
        }else{
            println("Muşteriniz bu ay ${quota - 50} GB aşım yapmıştır.")
            payment = (quota - 50) * 4 + 100
        }
            return payment
    }
}
```

```
fun main(){

    val e6 = InternetQuota()

    val input = Scanner(System.`in`)

    println("Müşteriniz kaç GB kullanmış ? ")

    val quota = input.nextInt()

    val result = e6.quotaCalculation(quota)


    println("Ödenecek tutar $result tl' dir.")
}
```

**Çıktı**
```
Müşteriniz kaç GB kullanmış ? 
82
Muşteriniz bu ay 32 GB aşım yapmıştır.
Ödenecek tutar 228 tl' dir.
```
</p>
</details>























































