# �N���X
class Player
  def method(input)
    puts input
  end
end

# �A�N�Z�T�̎��
attr_accessor :job # �I�u�W�F�N�g�O����ǂݏ����ł���
attr_reader   :job # �I�u�W�F�N�g�O����ǂݏo���݂̂ł���
attr_writer   :job # �I�u�W�F�N�g�O���珑���o���݂̂ł���

class Player
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
