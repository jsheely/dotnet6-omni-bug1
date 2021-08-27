# Reproduce Bug

- Open Project in VS Code
- Using dotnet core 6 preview 7
- Go to Constants.cs
- Attempt Find All References `shift-F12` on `MyText`
- Check output window for ominisharp error

```
[ERROR] FATAL UNHANDLED EXCEPTION: System.NullReferenceException: Object reference not set to an instance of an object
  at OmniSharp.Helpers.LocationExtensions+<>c.<GetQuickFix>b__0_2 (Microsoft.CodeAnalysis.Document document) [0x00000] in <d636994824794653bf410e4136f37a9c>:0 
  at System.Linq.Utilities+<>c__DisplayClass2_0`3[TSource,TMiddle,TResult].<CombineSelectors>b__0 (TSource x) [0x00012] in <9ba54d07696a449db4a4279fc05aa435>:0 
  at System.Linq.Enumerable+SelectArrayIterator`2[TSource,TResult].ToArray () [0x00012] in <9ba54d07696a449db4a4279fc05aa435>:0 
  at System.Linq.Enumerable.ToArray[TSource] (System.Collections.Generic.IEnumerable`1[T] source) [0x0001f] in <9ba54d07696a449db4a4279fc05aa435>:0 
  at OmniSharp.Helpers.LocationExtensions.GetQuickFix (Microsoft.CodeAnalysis.Location location, OmniSharp.OmniSharpWorkspace workspace) [0x00128] in <d636994824794653bf410e4136f37a9c>:0 
...
```