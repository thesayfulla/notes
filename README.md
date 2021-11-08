# only-git

`$ git checkout -b <branch_name>` — yangi branch yaratib unga o'tib oladi

`$ git add .` — file larni hammasi qo'shib yuboradi

`$ git add filename.txt` — 1ta file qo'shadi

`$ git commit -a` — commit qiladi message beradi add qilingan file uchun va *nano* yoki *vim* ni ishga tushirib yuboradi

`$ git commit -m "my message"` - 1ta line orqali commit qiladi message beradi add qilingan file uchun

`$ git checkout <branch_name>` — boshqa branchga o'tadi 

`$ git pull origin master` — remote branch dan pull oladi malumot olib keladi

`$ git checkout <branch_name>` — yana boshqa branchga o'tadi

`$ git rebase master` — master bilan rebase qiladi qo'shib yuboradi

`$ git push origin <branch_name>` — remotega push qilib yuboradi

`$ git remote` 
— remote ga ulangan narsalarni ko'rsatadi va odatda origin turgan bo'ladi

`$ git remote add <new_remote_name> <remote_url>.git`
 — yangi remote qo'shish uchun ishlatiladi

`$ git remote show <remote_name>` — remote origin haqida ma'lumot beradi

`$ git branch -d <branch_name>` — branch o'chirish

`$ git blame <filename>` — filedagi commitlar, kim yozgani, kim nima commit qilganini ko'rsatadi

`$ git log` — barcha loglar, commitlar listi

`$ git show <logid/tag>`
 — aynan o'sha logga tegishli o'zgarishlar qo'shilishlarni ko'rsatadi, commit message and more. . .

`$ git tag -l` — tag list(version list) 

`$ git clone <url>` — clone qilib oladi

## Redo commit <a href="https://stackoverflow.com/questions/2530060/in-plain-english-what-does-git-reset-do">url</a>
`$ git reset <commit>` - commit'ni orqaga qaytaradi(preserving changes locally, local saqlab qoladi)

`$ git reset --hard <commit>` - barchasini orqaga qaytaradi hech qanday saqlashlarsiz
