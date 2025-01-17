# Panduan GitHub Pages

Repository ini berisi panduan lengkap untuk membuat dan mempublikasikan proyek menggunakan **GitHub Pages**.

## Apa itu GitHub Pages?

[GitHub Pages](https://pages.github.com/) adalah layanan dari GitHub yang memungkinkan Anda mempublikasikan situs web langsung dari repository GitHub secara gratis.

---

## Langkah-langkah Membuat dan Mempublikasikan Proyek di GitHub Pages

### 1. Membuat Repository Baru di GitHub

- Masuk ke akun GitHub Anda.
- Klik tombol **+** di pojok kanan atas dan pilih **New repository**.
- Pilih nama repository, misalnya `panduan-github-pages`.
- Pilih visibilitas **Public**.
- Centang opsi **Initialize this repository with a README**.
- Klik **Create repository**.

### 2. Meng-upload File Proyek

Setelah repository dibuat, Anda bisa meng-upload file proyek ke dalam repository yang telah Anda buat. Berikut cara melakukannya:

- Buka halaman repository Anda.
- Klik tombol **Add file** dan pilih **Upload files**.
- Pilih file proyek yang ingin Anda upload (misalnya `index.html`, `style.css`, dan `script.js`).
- Klik **Commit changes** setelah file selesai di-upload.

### 3. Mengaktifkan GitHub Pages

Setelah file proyek berhasil di-upload, langkah selanjutnya adalah mengaktifkan GitHub Pages.

- Pergi ke halaman **Settings** dari repository Anda.
- Scroll ke bawah hingga bagian **GitHub Pages**.
- Pada bagian **Source**, pilih branch `main` atau `master` dan folder **/root**.
- Klik **Save**.

### 4. Akses Proyek Anda

Setelah GitHub Pages diaktifkan, Anda akan melihat URL yang dapat digunakan untuk mengakses situs web Anda, seperti:
https://<username>.github.io/<repository-name>/

Akses URL tersebut di browser untuk melihat proyek Anda online.

### 5. Memodifikasi dan Mengupdate Proyek

- Anda dapat memperbarui file proyek kapan saja dengan meng-upload file baru atau mengedit langsung melalui GitHub.
- Setelah melakukan perubahan, GitHub Pages akan memperbarui situs web Anda secara otomatis.

---

## Tips

- Pastikan file utama Anda adalah `index.html` agar GitHub Pages dapat memuat halaman utama dengan benar.
- Gunakan **Markdown** untuk menulis file README agar lebih mudah dipahami.

---

## Contoh File Proyek

Untuk membantu Anda memulai, berikut adalah contoh proyek HTML, CSS, dan JavaScript yang dapat Anda upload ke repository Anda:

### **File `index.html`**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Control Project</title>
  <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h1 class="text-center my-5">Kontrol Proyek</h1>
    <div class="row">
      <div class="col-md-6 mx-auto">
        <button id="controlBtn" class="btn btn-primary btn-block">Klik untuk Kontrol</button>
        <div id="status" class="alert alert-info mt-3" role="alert">
          Status: Tidak Aktif
        </div>
      </div>
    </div>
  </div>

  <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.3/dist/umd/popper.min.js"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
  <script src="script.js"></script>
</body>
</html>

### **File `style.css`**
```css
body {
  background-color: #f8f9fa;
  font-family: Arial, sans-serif;
}

#status {
  font-size: 1.2em;
  font-weight: bold;
}

### **File `script.js`**
```js
document.getElementById('controlBtn').addEventListener('click', function() {
  var statusDiv = document.getElementById('status');
  if (statusDiv.textContent.includes('Tidak Aktif')) {
    statusDiv.textContent = 'Status: Aktif';
    statusDiv.classList.remove('alert-info');
    statusDiv.classList.add('alert-success');
  } else {
    statusDiv.textContent = 'Status: Tidak Aktif';
    statusDiv.classList.remove('alert-success');
    statusDiv.classList.add('alert-info');
  }
});
