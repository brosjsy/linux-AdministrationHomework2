# linux-AdministrationHomework2

This repository contains solutions to tasks assigned in Homework 2 of the Practical Linux Administration course.

---

## 1. List files in your home directory by the last time they were modified

```bash
ls -lt ~
```

---

## 2–4. Move Characters to Their Directories

### Move jerry, george, kramer, and puddy to `seinfeld/`:
```bash
mv jerry george kramer puddy seinfeld/
```
![image](https://github.com/user-attachments/assets/3348d872-b5bb-430e-8347-22989bfc6d56)

### Move homer, bart, marge, lisa to `simpsons/`:
```bash
mv homer bart marge lisa simpsons/
```
![image](https://github.com/user-attachments/assets/5e6d5225-9dc0-4bd6-96ca-c8e47412964f)

### Move clark, luther, lois to `superman/`:
```bash
mv clark luther lois superman/
```
![image](https://github.com/user-attachments/assets/01ec1c7b-01d4-446a-9918-c0aac23e2ec6)

Verified directory structure:
![image](https://github.com/user-attachments/assets/0a7053aa-1dab-465b-95b7-b80169fdcac2)

---

## 5. Create Two New Files in `seinfeld/` Directory

```bash
cd seinfeld/
touch eliane newman
```
![image](https://github.com/user-attachments/assets/56cab1d3-edba-43f3-83d3-e524dfb3b716)

---

## 6. Change File Permissions

### Remove read access from everyone for `newman`:
```bash
chmod a-r newman
```
![image](https://github.com/user-attachments/assets/c871891c-04e2-4396-bf92-5cb58b210a99)

### Add write permission to group only for `eliane`:
```bash
chmod g+w eliane
```
![image](https://github.com/user-attachments/assets/1df2be15-c3f3-40da-8408-499fa1976340)

---

## 7. Become Root and Create Files in `superman/`

```bash
su
cd /home/<your-username>/superman
touch superman zad
```
![image](https://github.com/user-attachments/assets/fa0715fc-3012-48e2-990d-c4639c1be9fa)

---

## 8–9. Change File Ownership of `zad`

```bash
chown <your-username> zad
chgrp <your-username> zad
```
![image](https://github.com/user-attachments/assets/50276263-cd4b-4fa1-a10c-1760b2dc4054)

---

## 10. Output `dmesg` to a New File

```bash
cat /var/log/dmesg > ~/dmesg-new
```
![image](https://github.com/user-attachments/assets/97d0fbb5-ed15-41ea-b69f-cd97c0d05403)

---

## 11. View `dmesg-new` with `cat`, `more`, and `less`

```bash
cat dmesg-new | more
cat dmesg-new | less
```

<p float="left">
  <img src="https://github.com/user-attachments/assets/6ce3e43c-4700-460a-bbf2-f1f7c4f24245" width="200"/>
  <img src="https://github.com/user-attachments/assets/1f33f827-b6a2-4979-99d4-0c891cd149f1" width="200"/>
  <img src="https://github.com/user-attachments/assets/3759a2dc-c124-45e4-8d4b-6a2d7fcb47f6" width="200"/>
  <img src="https://github.com/user-attachments/assets/ca1a586e-3b6c-4005-9f9f-ee0042f07c9e" width="200"/>
</p>

---

## 12–13. View First/Last N Lines of `dmesg-new`

### First 10 lines to `dmesg-h10`:
```bash
head -n 10 dmesg-new > dmesg-h10
```

### Last 20 lines to `dmesg-t20`:
```bash
tail -n 20 dmesg-new > dmesg-t20
```
![image](https://github.com/user-attachments/assets/04b6ea2f-00d1-4367-831d-a0805fb3ba54)

---

## 14. Create Directory `seinfeld-characters` Inside `seinfeld/`

```bash
mkdir ~/seinfeld/seinfeld-characters
```
![image](https://github.com/user-attachments/assets/285cfc87-55a8-407a-a19f-01f28582b3de)

---

## 15. Add Text to `seinfeld-character` File (One Line Per Character)

```bash
echo -e "Jerry Seinfeld\nCosmo Kramer\nEliane Benes\nGeorge Costanza\nNewman Mailman\nFrank Costanza\nEstelle Costanza\nMorty Seinfeld\nHelen Seinfeld\nBabes Kramer\nAlton Benes\nJ Peterman\nGeorge Steinbrenner\nUncle Leo\nDavid Puddy\nJustin Pit\nKenny Bania" > seinfeld-character
```
![image](https://github.com/user-attachments/assets/4bf515d5-96ce-4be6-b1b5-d415b1b234d4)

---

## 16. Use `cut` and `awk` to Process `seinfeld-character`

### Use `cut` to get the first 4 letters and save to `filters-files`:
```bash
cut -c 1-4 seinfeld-character > filters-files
```

### Use `awk` to extract the second column:
```bash
awk '{print $2}' seinfeld-character >> filters-files
```

<p float="left">
  <img src="https://github.com/user-attachments/assets/9d7c20b5-847e-4ccb-8725-f33f06419072" width="200"/>
  <img src="https://github.com/user-attachments/assets/cc5d1e73-2cb2-4d45-9821-0d48502555ea" width="200"/>
  <img src="https://github.com/user-attachments/assets/582aafe7-9d66-4eb5-b6f2-af93f015fff2" width="200"/>
  <img src="https://github.com/user-attachments/assets/336f329c-6618-49ef-bb87-beed98f581ba" width="200"/>
</p>
