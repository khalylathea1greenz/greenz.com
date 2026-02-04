<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Green Z – Tukar Sampah Jadi Poin</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #f5f7f6; color: #1f2937; }
    header { background: #16a34a; color: white; padding: 24px; }
    section { padding: 24px; max-width: 1000px; margin: auto; }
    .card { background: white; padding: 20px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,.08); margin-bottom: 20px; }
    button { background: #16a34a; color: white; border: none; padding: 10px 16px; border-radius: 8px; cursor: pointer; }
    button:hover { background: #15803d; }
    input, select { padding: 8px; border-radius: 6px; border: 1px solid #d1d5db; }
    footer { background: #064e3b; color: #d1fae5; padding: 16px; text-align: center; }
  </style>
</head>
<body>
  <header>
    <h1>Green Z 🌱</h1>
    <p>Platform penukaran sampah jadi poin & nilai ekonomi</p>
  </header>

  <section>
    <div class="card">
      <h2>Tentang Green Z</h2>
      <p>Green Z adalah platform ekonomi digital yang mengubah sampah menjadi poin yang bisa ditukar uang atau sembako. Kamu setor sampah → ditimbang → dapat poin → ditukar 🎉</p>
    </div>

    <div class="card">
      <h2>Kalkulator Poin Sampah</h2>
      <label>Jenis Sampah:</label><br />
      <select id="jenis">
        <option value="5">Plastik (5 poin/gram)</option>
        <option value="3">Kertas (3 poin/gram)</option>
        <option value="8">Logam (8 poin/gram)</option>
      </select><br /><br />

      <label>Berat (gram):</label><br />
      <input type="number" id="berat" placeholder="contoh: 500" />
      <br /><br />
      <button onclick="hitungPoin()">Hitung Poin</button>
      <p id="hasil"></p>
    </div>

    <div class="card">
      <h2>Alur Green Z</h2>
      <ol>
        <li>Kumpulkan & pilah sampah</li>
        <li>Timbang di mitra Green Z</li>
        <li>Dapat poin otomatis</li>
        <li>Tukar poin jadi uang/sembako</li>
      </ol>
    </div>
  </section>

  <footer>
    <p>© 2026 Green Z | Ekonomi Digital Berbasis Lingkungan</p>
  </footer>

  <script>
    function hitungPoin() {
      const nilai = document.getElementById('jenis').value;
      const berat = document.getElementById('berat').value;
      if (!berat || berat <= 0) {
        document.getElementById('hasil').innerText = 'Masukkan berat yang valid ya 🙂';
        return;
      }
      const poin = nilai * berat;
      document.getElementById('hasil').innerText = `Total Poin: ${poin} poin`;
    }
  </script>
</body>
</html>

