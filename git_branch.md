# Git Branch
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