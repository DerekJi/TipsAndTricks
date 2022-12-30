# C# Format Date from Any formats


```c#

DateTime.ParseExact("18/09/2022", "dd/MM/yyyy", System.Globalization.CultureInfo.InvariantCulture).ToString("yyyy-MM-dd");

DateTime.ParseExact("20220918", "yyyyMMdd", System.Globalization.CultureInfo.InvariantCulture).ToString("yyyy-MM-dd");
```