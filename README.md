Nama   : Navyta Budi Yulia (312410184)

Kelas  : TI.24.A2 

# Lab5Web

# Pernyataan dan Tugas
1. Buat script untuk melakukan validasi pada isian form.

    ### 💻 Validasi Form Input

```html
<h3>Validasi Form Input</h3>

<form name="validasiForm" onsubmit="return validasi()">
    <p>Nama: <input type="text" name="nama" placeholder="Masukkan nama Anda"></p>
    <p>Email: <input type="text" name="email" placeholder="Masukkan email Anda"></p>
    <p>Pesan: <textarea name="pesan" placeholder="Tulis pesan Anda..."></textarea></p>
    <p><input type="submit" value="Kirim"></p>
</form>

<script>
    function validasi() {
        var nama = document.forms["validasiForm"]["nama"].value;
        var email = document.forms["validasiForm"]["email"].value;
        var pesan = document.forms["validasiForm"]["pesan"].value;

        if (nama == "" || email == "" || pesan == "") {
            alert("Semua kolom harus diisi!");
            return false;
        }

        // Cek format email sederhana
        var polaEmail = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;
        if (!email.match(polaEmail)) {
            alert("Format email tidak valid!");
            return false;
        }

        alert("Form berhasil dikirim!");
        return true;
    }
</script>

<img width="1920" height="1008" alt="Image" src="https://github.com/user-attachments/assets/530ad291-7805-406d-ae07-1027667f743d" />
