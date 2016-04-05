# Fsharp-Xamarin-desgin-lib-bug
A example project showing a binding a bug

The desing library has a resource id value named end. This breaks the F# compile step for the resource file
```
            // aapt resource value: 0x7f0a005c
            static member edit_query = 2131361884
            
            // aapt resource value: 0x7f0a0017
            static member end = 2131361815
            // manually adding ``<word>`` fixes the build issue.
            // static member ``end`` = 2131361815
            
            // aapt resource value: 0x7f0a007f
            static member end_padder = 2131361919
```
