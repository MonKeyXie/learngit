Git is a distributed version control system.
Git is a free software distributed under the GPL.
Git has a mutable index called stage
Git tracks changes.
Creating a new branch is quick and simple..
This is a small change

�����汾�⣺
��һ���������汾��-ѡ����ʵĵط���������Ŀ¼��
$ mkdir learngit
$ cd learngit
$ pwd		--pwd����������ʾ��ǰĿ¼��·������
ע��windows�²�Ҫ�����������ֿ�

�ڶ�����ͨ��git init��������Ŀ¼���Git���Թ���Ĳֿ⣺

$ git init	--��repository��������ʹ��

ע��windows�²�Ҫ�ü��±��༭.txt

�����������ļ���ӵ�repository
1.�����ϴ����ļ��ŵ��ֿ�(�磺learngit�ļ���)Ŀ¼��
2.$ git add readme.txt
3.git commit����Git�����ļ��ύ���ֿ⣺
  eg:$ git commit -m "wrote a readme file"
  -m����������Ǳ����ύ��˵��.

ʱ�⴩���(�޸�)��
git status�������������ʱ�����ղֿ⵱ǰ��״̬
git diff����������鿴�����޸ģ����Ѿ��ǲ����ϴ���ô�޸ĵ�readme.txt
�ύ�޸�Ҳ��git add ��git commit -m "�޸���Ϣ"

�汾���ˣ�
git log������ʾ�������ύ�ļ�¼(������ÿ���汾��commit id)
git log --pretty=oneline������ļ�Լ��
git reset����ѵ�ǰ�汾b���˵���һ���汾a
git reset --hard HEAD^ ��һ���汾����HEAD^������һ���汾����HEAD^^����Ȼ����100���汾д100��^�Ƚ�������������������д��HEAD~100

ȡ�����ˣ�
���˻غ����ˣ�ֻҪ����������д��ڻ�û�б��ص�����Ϳ���˳�������Ұ��Ұ����ҵ��Ǹ�b�汾��commit id��3628164...�����ǾͿ���ָ���ص�δ����ĳ���汾��
$ git reset --hard 3628164 �汾��û��Ҫдȫ��ǰ��λ�Ϳ����ˣ�Git���Զ�ȥ�ҡ�

git reflog������¼���ÿһ����������й�������������Ϳ����ҵ��汾b��commit id��