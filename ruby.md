# �N���X
```
class Name
  def method(input)
    puts input
  end
end
```

# �A�N�Z�T�̎��
* `attr_accessor :job`  �I�u�W�F�N�g�O����ǂݏ����ł���
* `attr_reader   :job`  �I�u�W�F�N�g�O����ǂݏo���݂̂ł���
* `attr_writer   :job`  �I�u�W�F�N�g�O���珑���o���݂̂ł���

```
class Player
  # �A�N�Z�T
  attr_accessor :power
  # �I�u�W�F�W�F�N�g�̏�����
  def initialize(job)
    # �C���X�^���X�ϐ�
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

# �N���X�ϐ�
`@@tax = 1.10` �錾�����C���X�^���X�S�Ăŋ��L�ł���ϐ�

```
class Food
  # �N���X�ϐ�
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

# �������z����I�u�W�F�N�g�ɂȂ��Ă���
```
text = "123"
p text.to_i 
p text.length
p text.class
p "123".class
p "a,b,c".split(",").length
```

# �N���X�̌p��
```
class Box
  # ���\�b�h�̃I�[�o�[���C�h
  def open()
    puts "Box"
  end
end

# �N���X�̌p��
class JewelryBox < Box
  def open()
    puts "JewelryBox"
  end
end
```
