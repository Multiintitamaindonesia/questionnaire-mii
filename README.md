# questionnaire-mii
Kuesioner Evaluasi Workshop MII
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MII Evaluasi Pelatihan</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 40px;
      background: #f5f5f5;
    }
    .container {
      max-width: 800px;
      background: #fff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      margin: auto;
    }
    h1, h2 {
      text-align: center;
    }
    label {
      font-weight: bold;
      display: block;
      margin-top: 20px;
    }
    textarea, input[type="text"] {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
    }
    .section {
      margin-top: 30px;
    }
    .options label {
      font-weight: normal;
      display: block;
      margin-left: 20px;
    }
    button {
      margin-top: 30px;
      padding: 12px 20px;
      background: #007BFF;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background: #0056b3;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Evaluasi Workshop Multi Intitama Indonesia </h1>
    <form onsubmit="sendWA(event)">
      <label>Judul Training:</label>
      <input type="text" id="judul" required>

      <label>Nama:</label>
      <input type="text" id="nama" required>

      <label>Perusahaan:</label>
      <input type="text" id="perusahaan">

      <div class="section">
        <h2>A. Materi Pelatihan</h2>
        <label>1. Seberapa relevan materi dengan kebutuhan Anda?</label>
        <div class="options">
          <label><input type="radio" name="q1" value="Sangat Relevan"> Sangat Relevan</label>
          <label><input type="radio" name="q1" value="Relevan"> Relevan</label>
          <label><input type="radio" name="q1" value="Cukup Relevan"> Cukup Relevan</label>
          <label><input type="radio" name="q1" value="Kurang Relevan"> Kurang Relevan</label>
          <label><input type="radio" name="q1" value="Tidak Relevan"> Tidak Relevan</label>
        </div>

        <label>2. Apakah materi mudah dipahami?</label>
        <div class="options">
          <label><input type="radio" name="q2" value="Sangat Mudah"> Sangat Mudah</label>
          <label><input type="radio" name="q2" value="Mudah"> Mudah</label>
          <label><input type="radio" name="q2" value="Cukup"> Cukup</label>
          <label><input type="radio" name="q2" value="Sulit"> Sulit</label>
          <label><input type="radio" name="q2" value="Sangat Sulit"> Sangat Sulit</label>
        </div>

        <label>3. Topik mana yang paling menarik?</label>
        <div class="options">
          <label><input type="checkbox" name="q3" value="Prosedur Ekspor-Impor"> Prosedur Ekspor-Impor</label>
          <label><input type="checkbox" name="q3" value="Dokumen dan Regulasi"> Dokumen dan Regulasi</label>
          <label><input type="checkbox" name="q3" value="Logistik dan Pengiriman"> Logistik dan Pengiriman</label>
          <label><input type="checkbox" name="q3" value="Strategi Pemasaran Internasional"> Strategi Pemasaran Internasional</label>
          <label>Lainnya: <input type="text" id="q3_lainnya"></label>
        </div>
      </div>

      <div class="section">
        <h2>B. Narasumber / Trainer</h2>
        <label>4. Apakah trainer menguasai materi?</label>
        <div class="options">
          <label><input type="radio" name="q4" value="Sangat Baik"> Sangat Baik</label>
          <label><input type="radio" name="q4" value="Baik"> Baik</label>
          <label><input type="radio" name="q4" value="Cukup"> Cukup</label>
          <label><input type="radio" name="q4" value="Kurang"> Kurang</label>
          <label><input type="radio" name="q4" value="Tidak Baik"> Tidak Baik</label>
        </div>

        <label>5. Cara penyampaian trainer?</label>
        <div class="options">
          <label><input type="radio" name="q5" value="Sangat Interaktif"> Sangat Interaktif</label>
          <label><input type="radio" name="q5" value="Interaktif"> Interaktif</label>
          <label><input type="radio" name="q5" value="Biasa Saja"> Biasa Saja</label>
          <label><input type="radio" name="q5" value="Kurang Interaktif"> Kurang Interaktif</label>
          <label><input type="radio" name="q5" value="Membosankan"> Membosankan</label>
        </div>
      </div>

      <div class="section">
        <h2>C. Fasilitas & Pelaksanaan</h2>
        <label>6. Fasilitas pelatihan?</label>
        <div class="options">
          <label><input type="radio" name="q6" value="Sangat Memadai"> Sangat Memadai</label>
          <label><input type="radio" name="q6" value="Memadai"> Memadai</label>
          <label><input type="radio" name="q6" value="Cukup"> Cukup</label>
          <label><input type="radio" name="q6" value="Kurang"> Kurang</label>
          <label><input type="radio" name="q6" value="Tidak Memadai"> Tidak Memadai</label>
        </div>

        <label>7. Pelaksanaan keseluruhan?</label>
        <div class="options">
          <label><input type="radio" name="q7" value="Sangat Baik"> Sangat Baik</label>
          <label><input type="radio" name="q7" value="Baik"> Baik</label>
          <label><input type="radio" name="q7" value="Cukup"> Cukup</label>
          <label><input type="radio" name="q7" value="Kurang"> Kurang</label>
          <label><input type="radio" name="q7" value="Tidak Baik"> Tidak Baik</label>
        </div>
      </div>

      <div class="section">
        <h2>D. Manfaat dan Saran</h2>
        <label>8. Seberapa besar manfaat pelatihan ini?</label>
        <div class="options">
          <label><input type="radio" name="q8" value="Sangat Besar"> Sangat Besar</label>
          <label><input type="radio" name="q8" value="Besar"> Besar</label>
          <label><input type="radio" name="q8" value="Cukup"> Cukup</label>
          <label><input type="radio" name="q8" value="Kecil"> Kecil</label>
          <label><input type="radio" name="q8" value="Tidak Ada"> Tidak Ada</label>
        </div>

        <label>9. Berminat ikut pelatihan lanjutan?</label>
        <div class="options">
          <label><input type="radio" name="q9" value="Ya"> Ya</label>
          <label><input type="radio" name="q9" value="Tidak"> Tidak</label>
        </div>

        <label>10. Saran / Masukan:</label>
        <textarea id="saran" rows="4"></textarea>
      </div>

      <button type="submit">Kirim via WhatsApp</button>
    </form>
  </div>

  <script>
    function sendWA(e) {
      e.preventDefault();
      const nama = document.getElementById('nama').value;
      const judul = document.getElementById('judul').value;
      const perusahaan = document.getElementById('perusahaan').value;
      const saran = document.getElementById('saran').value;
      const lainnya = document.getElementById('q3_lainnya').value;

      const radioValues = (names) => names.map(name => {
        const el = document.querySelector(`input[name='${name}']:checked`);
        return el ? `${name}: ${el.value}` : `${name}: -`;
      }).join("\n");

      const q3s = [...document.querySelectorAll("input[name='q3']:checked")].map(cb => cb.value);
      if (lainnya) q3s.push("Lainnya: " + lainnya);

      const message = `Evaluasi Pelatihan\n\nJudul: ${judul}\nNama: ${nama}\nPerusahaan: ${perusahaan}\n\n` +
        radioValues(["q1","q2","q4","q5","q6","q7","q8","q9"]) +
        `\nTopik Menarik: ${q3s.join(", ")}\nSaran: ${saran}`;

      const encoded = encodeURIComponent(message);
      window.open(`https://wa.me/6281219192238?text=${encoded}`, '_blank');
    }
  </script>
</body>
</html>
