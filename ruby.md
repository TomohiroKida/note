# クラス
```
class Name
  def method(input)
    puts input
  end
end
```

# アクセサの種類
* `attr_accessor :job`  オブジェクト外から読み書きできる
* `attr_reader   :job`  オブジェクト外から読み出しのみできる
* `attr_writer   :job`  オブジェクト外から書き出しのみできる

```
class Player
  # アクセサ
  attr_accessor :power
  # オブジェジェクトの初期化
  def initialize(job)
    # インスタンス変数
    @job = job
  end
  def walk()
    puts "#{@job}"
  end
end
player1 = Player.new("solder")
player1.walk()
puts player1.power
player1.power = 1
```

# クラス変数
`@@tax = 1.10` 宣言したインスタンス全てで共有できる変数

```
class Food
  # クラス変数
  @@tax = 1.10
  def initialize(price)
    @price = price
  end
  def pay()
    @price * @@tax
  end
end
a = Food(100)
b = Food(200)
puts a.pay + b.pay
```

# 文字列や配列もオブジェクトになっている
```
text = "123"
p text.to_i 
p text.length
p text.class
p "123".class
p "a,b,c".split(",").length
```

# クラスの継承
```
class Box
  # メソッドのオーバーライド
  def open()
    puts "Box"
  end
end

# クラスの継承
class JewelryBox < Box
  def open()
    puts "JewelryBox"
  end
end
```
