### Cara daftar github
1. Buka https://github.com
2. Input username, email dan password.
3. Klik sign up.

### Cara Setup SSH di Github
#### Cara Generate SSH key
1. Buka terminal
2. Ketik perintah berikut
'''
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
'''
3. Saat ada perintah  "Enter a file in which to save the key," Tekan enter saja.
4. Kemudian isikan password SSH key nya dan enter.

#### Menambahkan SSH key ke SSH Agent
1. Jalankan perintah berikut
'''
$ eval "$(ssh-agent -s)"
'''
2. Masukkan SSH key ke SSH Agent dengan perintah berikut.
'''
$ ssh-add ~/.ssh/id_rsa
'''
3. Copy isi SSH key dengan perintah berikut.
'''
$ clip < ~/.ssh/id_rsa.pub
'''

#### Menambahkan SSH key ke Akun Github
1. Login akun github.
2. Masuk ke menu setting dan pilih menu SSH and GPG Key.
3. Klik tombol new SSH key.
4. Isikan title dan kemudian paste-kan SSH key yg sudah di copy tadi.

### Membuat repo
1. Login akun github.
2. Klik Create New Repository.
3. Isi nama repository-nya beserta deskripsinya.
4. Pilih private jika tidak ingin dilihat orang lain atau pilih public jika ingin repo nya bisa dilihatbkrang lain.

### cara push ke remote repo
1. Buka terminal.
2. Ketik 'mkdir nama-repo' kemudian ketik 'cd nama-repo'.
3. Ketik perintah berikut untuk membuat file Readme.md di local komputer.
'''
$ echo "#nama-repo" >> README.md
'''
4. Kemudian ketik 'git init'.
5. Ketik '$ git add README.md' untuk menambahkan file README.md.
6. Ketik '$ git commit -m "Commit Pertama"' untuk melakukan kommit pertama ke dalam repo.
7. Ketik '$ git remote add origin git@github.com:akun/nama-repo.git'.
8. Ketik '$ git push -u origin master'.
