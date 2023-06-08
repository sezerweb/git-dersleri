# Git Temelleri
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
   git commit -a -m "ilk commit de olur": ile add ve commit işlemini aynı anda yaptım
4. Git Log  
   git log : commitleri görebiliriz
   git bash ekranında uzun commit sırası olunca oklarla gezin q ile çık
5. Gitignore
   .gitignore   dosyaı oluşturup içine takip edilmemesini istediğiniz dosya ya da klasörleri ekleriz
   
   
      