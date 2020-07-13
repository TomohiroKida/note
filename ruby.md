# クラス
class Player
  def method(input)
    puts input
  end
end

# アクセサの種類
attr_accessor :job # オブジェクト外から読み書きできる
attr_reader   :job # オブジェクト外から読み出しのみできる
attr_writer   :job # オブジェクト外から書き出しのみできる

class Player
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
