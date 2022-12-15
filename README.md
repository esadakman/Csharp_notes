# CSharp_notes

<!-- ## extra_notlar

 -->

- Youtube üzerinde 'Yazılım Teknolojileri Akademisi' tarafından yayınlanmış olan 'C# Dersleri' başlıklı video serisini izlerken almış olduğum çalışma notlarım.

İlgili video serisine [buradan](https://www.youtube.com/watch?v=3t0rU5Yo4nM&list=PLi1BmHvgBkxIYweLR52cRJnit4AEEugn4) ulaşabilirsiniz.

## session_001_Visual_Studio_Notları:

- Yorum kısayolu (ctrl+k) + (ctrl+C) veya manuel olarak `//` yazarak tek satırı, `/* text */` diyerek birden fazla satırı yoruma alabiliriz.
- (ctrl+k) + (ctrl+u) tuşlarıyla ile de uncomment yapabiliriz.
- (ctrl+k) + (ctrl+D) tuşlarına basarak bütün sayfayı düzenleyebiliriz. (formatter)
- (Shift + Alt + '.'): Seçili yerin (varsa) bir sonraki tekrarını seçer
- (Shift + Alt + ','): Seçili yerin (varsa) bütün tekrarlarını seçer
- Solution Explorer kısayolu (ctrl+Alt+L)
- Toolbox Explorer kısayolu (ctrl+Alt+X)
- Eklemeyi istediğimiz tool'ları toolbox'dan seçip sürükleyerek formumuza ekleyebiliriz
- comboBox html'de ki select tag'ine benzer.
- ComboBox sınıfı, yöntemini kullanarak IndexOf belirtilen nesneyi arar.
- comboBoxNames.Items.Add diyerek comboBox'a item ekleyebiliriz
- SelectedItemComboBox , bu nesneyi listede o anda seçili olan nesne yapmaya çalışır.

#### VSCode_Notları

- 'dotnet --help' komutunu console'a yazarakdotnet sürümümü kontrol edebilirim.
- 'dotnet new console' komutunu console'a yazarak basit bir console projesi oluşrurabiliriz.
- 'dotnet run' komutunu console'a yazarak ise console projemizi çalışrıtabiliriz.

## session_002_GUI_Window_Forms Notları:

- labelWrittenName.Text diyerek oluşturduğumuz label'a dinamik olarak text yazdırabiliriz
- dateTimePicker ile tarih seçici ekleyebiliriz
- trackBarVolume ile'de trackBar seçeneği ekleyebiliriz
- Eklenen ögelerin yeni satırda eklenmesi için '\n' ifadesini ekliyebiliriz

## session_003_RadioButton_CheckBox_Panel

- Radio button'ın checkbox'tan farkı sadece bir tanesinin seçilebilmesidir
- Radio button'ın default seçili gelmesi için ise 'Checked' kısmını true yapmamız gerekiyor
- Projeyi çalıştırırken bazen değişiklikler anında gözükmeyebiliyor. öyle bir durumda 'Build' kısmından 'Clean Solution' deyip tekrar çalıştırmalıyız
- Panel kullanarak ekranımı bölebilir, çeşitli customization'lar yapabilirim
- herhangi bir eventi kaldırmak istediğimiz zaman öncelikle ilgili kod satırını silmemiz, ardından ise solution explorerda yer alan Designer'ın üzerine çift tıklayıp hata veren satırları siliyoruz

## session_004_Variables_Data_Types

- Değişken tanımlarken void dışında tanımlarsak Form1 classında ki diğer yerlerde de kullanabiliriz.
- Değişkenler'i Tek satırda tanımlayabileceğim gibi iki ayrı satırda da tanımlayabilirim
  `string isim; 
isim = textBox1.Text;`
- String istenen yere integer yazdığımız zaman bu veriyi kullanmak istersek int'e çevirmemiz gerekiyor, bunun için Convert.ToInt16(var_name) veya Int16.Parse(var_name) metodlarını kullanabiliriz
- Integer'a çevirmek için ise Convert.ToString(var_name) veya ToString(var_name) metodlarını kullanabiliriz

## session_005_Data_Types \_Float_DoubleChar

- float: 7 decimal digits, double: 15 decimal digits alır
- float ile sayı tanımlarken sonuna 'f' eklemek gerekir, `float x = 5.123456789f;`
- double'ı kullanırken sonuna herhangi bir harf yazmamıza gerek yok fakat double daha fazla yer kaplar.
- Char veri türü, Unicode standardında eşdeğer karakterler içeren 16 bitlik bir veri türüdür. Her karakterin Unicode standart çerçevesinde karşılık gelen bir karakteri vardır ve char türüne bir değişken değeri atadıktan sonra bir karakteri temsil eder.
- char tanımlarken tek tırnak olarak tanımlamamız gerekir

## session_006_Arithmetic_Operations

- Formda boş bir yere tıklayarak form ismini ve iconu gibi özellikleri değiştirebiliriz
- Bir sayının üssünü almak için Math.Pow func. kullanabiliriz.
- Fakat Math.Pow() double döndüğü için ya sonucu (int) diyerek integere'a çeviririz ya da değişkenimizi double olarak belirleriz

<!-- ## session_007_Geometric_Calculator  -->

## session_008_Functions

- Fonksiyonlar yazılırken `public`, `private` ve de `protected` olmak üzere üç gizlilik seviyesinde yazılır.
- Private => Sadece aynı class içerisinde çağrılabilir. Sadece belirtilen işlemi yaptığı ve herhangi bir şey döndürmediği için 'void' denir.
- Fonksiyon isminin üstüne gelip f12'ye basarsak fonksiyonun tanımlandığı yere gidebiliriz

## session_009_if_else

- && operatörü “ve” anlamındadır
- || operatörü “veya” anlamındadır

```cSharp
if (ort >= 50)
Console.WriteLine("Dersten Geçtiniz.");
else
Console.WriteLine("Dersten Kaldınız.");
```

## session_010_Switch_Case

- JavaScript'ten farklı olarak burda her case'de break yazmamız gerekiyor.
- String interpolation using :

```cSharp
string name = "Mark";
var date = DateTime.Now;
// Composite formatting:
Console.WriteLine("Hello, {0}! Today is {1}, it's {2:HH:mm} now.", name, date.DayOfWeek, date);
// String interpolation:
Console.WriteLine($"Hello, {name}! Today is {date.DayOfWeek}, it's {date:HH:mm} now.");
// Both calls produce the same output that is similar to:
// Hello, Mark! Today is Wednesday, it's 19:40 now.
```

## session_011_Operators_Boolean

- && and, || or
- `x == 5` eşitlik durumuna bakar, `x != 5` eşit olmama durumuna bakar.
- `x = 5` dersek atama yapar.

## session_012_for_loop

- For loop içerisinde tek satır kod yazacaksak süslü parantez açmamıza gerek yok

```cSharp
 for (int i = 0; i <= 10; i++)
   Console.WriteLine(i);
```

## session_014_While_Do_While

- While

```cSharp
  int i = 0; // for'dan farklı olarak değişkenimi while'dan önce tanımlamam gerekiyor
  // while kullanırken temporary değişkenimi while parantezi içinde belirtiyorum
  while (i < 5)
  {
    Console.WriteLine(i);
    i++;
  }
```

- Do While

```cSharp
  int i = 0;
  do // Do while'ın while'dan farkı do'da ki işlemi en az 1 kere yapar daha sonra while koşulunu kontrol eder
  {
      Console.WriteLine("i = {0}", i);
      i++;
  } while (i < 5);
```

<!-- ## session_015_Quiz -->

## session_016_Timer_Progress_Bar

- Timer componenti ekranda görünmez ama arka planda çalışır .
- Properties kısmından enabled'ı true yaparsak program çalışır çalışmaz Timer'ımız çalışmaya başlar.
- Interval kısmından ise timer'ı çağıracağımız zaman aralığını belirleyebiliriz
- Yine properties kısmından Events'e gelerek behavior kısmına çift tıklıyarak bir timer_tick fonksiyonu oluşturabiliriz. (Start ve Stop fonksiyonlarıyla timer'ı yönetibiliriz)

## session_017_Array

- Birden fazla aynı tipte veriyi tek bir değişkende toplayan verilere array denir
- Bir array oluştururken değişken oluştururkende yaptığımız gibi önce tipini belirtmemiz gerekiyor.

```CSharp
  int[] array = { 7, 12, 25, 34, 46 };
  string[] employees = { "Michael", "Dwight", "Jim", "Pam", "Creed" };
```

## session_018_Foreach

- for each kullanırken arraylere indexle erişmek zorunda değiliz. Iteratorla erişebiliriz.
```CSharp
  string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
  foreach (string i in cars)
  {
    Console.WriteLine(i);
  }
``` 

## session_019_CSharp_Console
- Çalıştığımız projeyi konsolda kullanmak istiyorsak; 
- Proje ismine sağ tıklayıp properties'e geliyoruz
- Outpu Type'ı Console Application olarak değiştiriyoruz
- İnput gitmek için ise `Console.ReadLine`'ı kullanabiliriz. (Int'e çevirmeyi unutmamalıyız) 
