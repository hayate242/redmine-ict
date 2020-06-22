# redmine-ict
```
docker-compose exec redmine bash
ssh-keygen -t rsa -C sippu242@gmail.com
cat /root/.ssh/id_rsa.pub
-> githubに公開鍵を登録
cp /root/.ssh/id_rsa /home/redmine/.ssh/id_rsa
chown redmine:redmine /home/redmine/.ssh/id_rsa

------- 以下redmineユーザで作業 -----------
su - redmine
chown redmine:redmine repositories/

----- repositoryをbareでclone ----------
cd /usr/src/redmine/repositories/
git clone --bare git@github.com:ictc/mima-community-bus-pbl2020.git

----- 手動更新 ---------
cd /usr/src/redmine/repositories/mima-community-bus-pbl2020.git
git fetch origin 'refs/heads/*:refs/heads/*'
```
### github-webhook

プロジェクトID確認方法
```http://pbl.ict.ehime-u.ac.jp:8000/projects.xml?limit=100```
にアクセスする！


