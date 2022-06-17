1. class 與 struct 差別

結構（Struct）
是一種實質型別（Value Type）。
存放在記憶體的Stack區。
不需要使用new就可以產生一份新的Struct。
若裡面有N個欄位，那麼一定要把N個欄位填滿，這個Struct才可以開始被使用。
不能擁有空參數的建構子（Constructor），若一定要寫建構子，則在建構子內要把所有欄位都指派值進去。
欄位不可以使用初始化賦值，請走建構子一途。

類別（Class）
是一種參考型別（Reference Type）。
存放在記憶體的Heap區。
一定要使用new來產生一份新的Instance。
若裡面有N個欄位，那麼不需要把N個欄位填滿，這個Instance才可以開始被使用。
能購擁有空參數的建構子（Constructor）。
欄位可以使用初始化賦值，例如：public string cName = "尚未命名";。

使用「Stack」來存放的結構（Struct），在進行耗用大量記憶體來存放「資料」時，基本上完全不會產生記憶體碎片化的問題，且在Struct離開Function時，這些記憶體會馬上被Release出去，讓系統的記憶體佔用率極低。
使用「Heap」來存放的類別（Class），在進行耗用大量記憶體來存放「資料」時，在那邊參考來參考去，不僅造成碎片化，且當程式設計師忘記把Reference釋出（Dispose、Null），這些被佔用的記憶體甚至等到整個程式的生命週期結束後都不見得會被釋放掉（Release）。

2. optional
optional 的變數(常數)，可以被設定為 nil，表示它處於無值的狀態，不管它的型別是什麼
在宣告變數(常數)時，於型別的後頭接上問號，即表示它是一個 optional 變數(常數)。

weak 當參照被釋放的時候會將該參數設為nil 
