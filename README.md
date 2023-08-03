# MYSQL DATABASE EXPORT/Namecheap IMPORT
1. In mysql workbench leftclick on db and select alter database, convert database to plain basic utf8. Namecheap uses an older version and the latest whatever collation will not work.
2. Edit the imported sql file with text editor and change instances of - Find ‘utf8mb4_0900_ai_ci’ & replace it with ‘utf8mb4_unicode_ci’. 
https://meetanshi.com/blog/error-1273-unknown-collation-utf8mb4-0900-ai-ci-in-mysql/
3. In namecheap phpMyAdmin import, and select file...should upload and create db/tables with no issue now

# Depoly Node app to namecheap
https://www.youtube.com/watch?v=qGvteC3dZnk
1. zip all files except nodemodules and .git files
2. go to filemanager folder created during nodejs app creation, delete all auto generated files, upload zip, extract zip and delete zip to cleanup
3. Go back to node application, Run npm install bc package.json is now in file manager folder - NOTE- MAY NEED TO EXIT & REENTER node applications view 