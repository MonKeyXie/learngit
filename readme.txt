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

���������ݴ�����
�ɸ����ļ��ǹ�������ģ���.txt�ļ�
�汾����� �ݴ��� �� ��֧master�Ѿ�HEAD
git addʱ���޸ļӵ�������(stage)��git commitʱ��stage��������ύ����ǰbranch

�����޸ģ�
Git�������汾����ϵͳ��Ƶ����㣬��ΪGit���ٲ���������޸ģ������ļ���

�����޸ģ�
��ûgit add����������git checkout -- file�����Զ������������޸�
�Ѿ�git add����������git reset HEAD file���԰��ݴ������޸ĳ�������unstage�������·Żع���������git checkout --file

ɾ���ļ���
ȷʵҪ�Ӱ汾����ɾ�����ļ����Ǿ�������git rm fileɾ��������git commit
��һ�������ɾ���ˣ���Ϊ�汾���ﻹ���أ����Կ��Ժ����ɵذ���ɾ���ļ��ָ������°汾��
$ git checkout -- test.txt
git checkout��ʵ���ð汾����İ汾�滻�������İ汾�����۹��������޸Ļ���ɾ���������ԡ�һ����ԭ����

���Զ�̿⣺
Create a new repo����ť������һ���µĲֿ⡣
Repository name����learngit����������Ĭ�����ã������Create repository����ť���ͳɹ��ش�����һ���µ�Git�ֿ�
�ڱ��ص�learngit�ֿ����������
$ git remote add origin git@github.com:MonKeyXie/learngit.git
��Ӻ�Զ�̿�����־���origin������GitĬ�ϵĽз���Ҳ���Ըĳɱ�ģ�����origin�������һ����֪����Զ�̿⡣

���͵�ǰ��֧��
����Զ�̿��ǿյģ����ǵ�һ������master��֧ʱ��������-u������Git������ѱ��ص�master��֧�������͵�Զ���µ�master��֧������ѱ��ص�master��֧��Զ�̵�master��֧�������������Ժ�����ͻ�����ȡʱ�Ϳ��Լ����
$ git push -u origin master	��һ������
$ git push origin master	��������

cloneԶ�̿⣺
����һ���µĲֿ⣬���ֽ�gitskills�����ǹ�ѡInitialize this repository with a README������GitHub���Զ�Ϊ���Ǵ���һ��README.md�ļ���
������������git clone��¡һ�����ؿ⣺
$ git clone git@github.com:MonKeyXie/gitskills.git
��������https://github.com/MonKeyXie/gitskills.git�����ĵ�ַ��ʵ���ϣ�Git֧�ֶ���Э�飬Ĭ�ϵ�git://ʹ��ssh����Ҳ����ʹ��https������Э�顣

