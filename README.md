# BTK Akademi
[Versiyon Kontrolleri: Git ve GitHub](https://www.btkakademi.gov.tr/portal/course/versiyon-kontrolleri-git-ve-github-19439)

## Giriş ve Kurulumlar
1. Git ve Github.com nedir.
2. Git kurulumu  
master mı, main mi
3. Terminal Kullanımı  
   ls, pwd (print working directory), cd (change directory), cd .., clear, mkdir (make directory), touch : doysa oluştur, cat dosyaya bak, rm dosya kaldır, rm -rf klasörü kaldır
4. Kullanıcı Adı ve Email Bilgileri girmek  
   git config --global user.name "sezerweb"  
   git config --global user.email "sezer.akbulut@uzmar.net"  
   git config user.name 
---
## Git Temelleri
1. Git Görselleştirme  
   commit, branch  
   çalışma klasörü: çalışılan yer   
   index-staging: commit öncesi alan git add .   
   local repository: commit sonrası alana

   commit öncesi, git add ile çalışma klasöründen --> index-staging bölümüne aktarılır, commit edince local repositorye gider.
2. Git init ve Status  
   git status:klasörün durumu gösterir  
   git init:giti başlatmış oluruz.
3. İlk Commit  
   git add . ya da   : staging bölümüne attık  
   git restore --staged xxxfile.txt  ya da git restore --staged . : stagingden geri alabiliriz  
   git commit -m "ilk commitim bu"  
   git commit -a -m "ilk commit de olur": ile add ve commit işlemini aynı anda yaptım ama daha önce add yapılmışsa.
4. Git Log  
   git log : commitleri görebiliriz
   git bash ekranında uzun commit sırası olunca oklarla gezin q ile çık
5. Gitignore
   .gitignore   dosyaı oluşturup içine takip edilmemesini istediğiniz dosya ya da klasörleri ekleriz
--- 
## Git Branch
1. HEAD nedir?  
   Genelde son commiti gösterir, güncel olarak nerede olduğumuz gösterir
2. Merge  
   git branch : branchları listele    
   git branch xxx: yeni branch açar  
   git switch xxx: xxx branch geç  
   önce mastera geç sonra merge et  
   git merge xxx
3. Fast Forward  
   ayrı branchta bişeyler yaptık ama masterda hiç değişiklik olmazda yani aslında yeni brancha ihtiyaç yokmuş, mege edince fast forwarding oluyor.
4. Merge Conflict  
   branchlar arasında aynı dosya üzerinde değişiklik yapılırsa.
5. Stash  ve Pop   
   commmit etmeden durummu saklamak için yapılır. çalışma klasörü, index ya da local repository dışında ayrı bir yere konulur. Yarım işler için ara bir yer gibi.  
   git stash ile oluşur, git stash pop ile geri getirilir listeden kaldır, git stash list ile listeler.     
   stash@{0}: sdffsdfs.. 98989sdfj67 açıklama...  
   stash@{1}: sdffsdfs.. 98989sdfj67 açıklama...     
   git stash apply stash@{1}  listede kalır    
   git stash clear ile temizlerim
---   
## Geçmişe Dönme
1. Checkout    
   git log sonrası gelen listedeki commitlerin hash kodu ile istediğimiz commite geri dönebiliriz.  
   git checkout 1f1a1ee9090d19ad37a8d4d83828b30e90a3597d  gibi  
   kafayı kopardık burada incelme işlemi sonrası mastera dönebiliriz ya da yeni bir branch oluşturup oradan devam edebiliriz daha sonra masterla merge ederiz.
2. Reset vs Revert
   git reset 1f1a1ee9090d19ad37a8d4d83828b30e90a3597d ile döndüğümüz commiten sonraki commitleri siliyor ama değişiklikler duruyor, git reset --hard 1f1a1ee9090d19ad37a8d4d83828b30e90a3597d dersek değişiklikleri de siliyor.
   git log kayıtlarını düzenlemiş oluyoruz.  
   git revert 1f1a1ee9090d19ad37a8d4d83828b30e90a3597d ilgili commiti geri aldım ama aynı branchdan devam ettim, tarihçe bozulmadı. ama geri almış oldum. geri aldığım commit duruyor ama. 
3. Git Diff  
   farkları gösterir 
   git diff o ana yapılmış ama add yapılmamış dosya farklılıklarını gösterir.  
   git diff HEAD  
   git diff 1f1a1e 90d19ad diyerek iki commit arasındaki farkı görürüz
   git diff master feat  iki branch arasındaki farkları görürüz   

4. Rebase   
   Masterdan ayrı bir branchla çalışırken, masterda değişilik olabilir, conflict olmamasına rağmen kendi branchımızla merge etmek isteyebiliriz. Bu şekilde bir çok kez merge yapılabilir ve git tarihçiseninde bir sürü gereksiz merge logu oluşur. Tarihçeyi mergelerden temizlemek için yapılabilir ama daha önce başkaları ile kendi branchlarımı paylaşmamışsam.
   git rebase master  : bulunduğum branchdaki merge commitleri vs temizler, ve sıralar.. mater ve sonrasında diğer branch commitlerini sıralar.



## Notlar:
   git config --global core.editor "nano" : editörü değiştir.  
   git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
