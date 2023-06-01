# BASIC ROS
## Membuat Workspace
1. Buat folder baru yang akan dijadikan workspace.
2. Buat folder dengan nama `src` didalam folder workspace.
3. Ketik command `catkin_make` pada directory workspace melalui terminal.
4. Ketik command `source devel/setup.bash` pada directory workspace melalui terminal.

## Membuat Package
1. Ketik command berikut pada directory `nama_workspace/src`.
```
$ catkin_create_pkg nama_package [depend1 depend2 ...]
```
2. Ketik kedua command berikut pada directory `nama_workspace` untuk *build* ulang workspace.
```
$ catkin_make
$ source devel/setup.bash
```

## Membuat File Message
1. Buat folder dengan nama `msg` didalam folder `nama_package`.
2. Buat file dengan ekstensi `.msg` didalam folder `msg`.
3. Isi file tersebut dengan format sebagai berikut.
```
tipedata pesan1
tipedata pesan2
```

## Membuat File Service
1. Buat folder dengan nama `srv` didalam folder `nama_package`.
2. Buat file dengan ekstensi `.srv` didalam folder `srv`.
3. Isi file tersebut dengan format sebagai berikut.
```
tipedata nama_var_req1
tipedata nama_var_req2
---
tipedata nama_var_res1
tipedata nama_var_res2
```

## CMakeLists.txt
*untuk petunjuk yang lebih jelas, dapat melihat langsung penjelasan yang berada di file CMakeLists.txt*
- Inisialisasi nama package (nama folder tidak selalu merupakan nama package).
```
project(...)
```
- Menambahkan file message yang berada di dalam folder `msg`.
```
add_message_files(
   FILES
   abc.msg
)
```
- Menambahkan file service yang berada di dalam folder `srv`.
```
add_service_files(
   FILES
   abc.srv
)
```
- Menambahkan file action yang berada di dalam folder `action`.
```
add_action_files(
   FILES
   abc.action
)
```
