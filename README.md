<html>
  <head>
    <title>Abdul Prayogi</title>
    <h1 style="color:rgb(255, 0, 0)"><marquee>Cashier Program By Abdul Prayogi</marquee></h1><hr>
  </head>
  <body style="background-color: rgb(236, 223, 229);">
    <center>

    <h2 style="color:"green"> Daftar Harga Buah-Buahan</h2>
    
      <ul style="list-style: none;">
      <li>
        <b>Apel : 23.000
     /kg
      </li>
       <li>
        Pisang : 12.000
        <small>/kg</small>
      </li>
       <li>
        Anggur : 35.000
        <small>/kg</small>
      </li>
       <li>
        Mangga : 17.000
        <small>/kg</small>
      </li>
       <li>
        Jambu : 25.000
        <small>/kg</small>
      </li>
      <li>
        Jeruk : 30.000
        <small>/kg</small>
      </li>
      <li>
        Naga : 27.000
        <small>/kg</small>
      </li>
      <li>
        Kelapa : 70.000
        <small>/kg</small>
      </li>
      <li>
        Semangka : 45.000
        <small>/kg</small>
      </li></b>
    </ul>
     

    <hr>
    <label for="buah"> Jenis-Jenis Buah :</label>
    <select id="buah">
      <option value="Apel">Apel</option>
      <option value="Pisang">pisang</option>
      <option value="Anggur">anggur</option>
      <option value="Mangga">mangga</option>
      <option value="Jambu">Jambu</option>
      <option value="Jeruk">jeruk</option>
      <option value="Naga">Naga</option>
      <option value="Kelapa">Kelapa</option>
      <option value="Semangka">Semangka</option>
    </select>
    <br>
    <br>
    <input type="number" id="kilo" placeholder="Masukkan Jumlah Buah/Kilogram" style="width:250px; height:35px">
    <input type="number" id="diskon" placeholder="Masukkan jumlah Diskon (0%-100%)" style="width:250px; height:35px">
    <br>
    <br>
    <button onclick="proses()">Total</button>
    <hr>
    <h1 style="color:green;">RESULT</h1>
    <p id="total">..</p>
  </center>

    <script>
      function proses () {
        var buah = document.getElementById('buah').value;
        var kilo = document.getElementById('kilo').value;
        var diskon = document.getElementById('diskon').value;
        total(buah,kilo,diskon);
      }

      function total (buah,kilo,diskon) {
        var hargaBuah = getHargaBuah(buah);
        document.getElementById('total').innerHTML = ("jenis buah : " + buah + "<br>");
        document.getElementById('total').innerHTML += ("harga buah/kg : Rp" + hargaBuah + "<br>");
        document.getElementById('total').innerHTML += ("jumlah kg :" + kilo + "kg<br>");
        document.getElementById('total').innerHTML += ("potongan diskon :" + diskon + "%<br>");
        document.getElementById('total').innerHTML += ("besar diskon : Rp" + (diskon/100) * (hargaBuah*kilo) + "<br>");
        document.getElementById('total').innerHTML += ("<br>Sub Total : Rp" + (hargaBuah*kilo) + "<br>");
        document.getElementById('total').innerHTML += ("total : Rp" + ((hargaBuah*kilo) - (diskon/100)*(hargaBuah*kilo)));
      }
      function getHargaBuah(buah) {
        var hargaBuah;
        if (buah=='Apel') {
          hargaBuah="23000"
        }
        else if (buah=='Pisang') {
          hargaBuah="12000"
        }
        else if (buah=='Anggur') {
          hargaBuah="35000"
        }
       else if (buah=='Mangga') {
          hargaBuah="17000"
        }
        else if (buah=='Jambu') {
          hargaBuah="25000"
        }
        else if (buah=='Jeruk') {
          hargaBuah="30000"
        }
        else if (buah=='Naga') {
          hargaBuah="27000"
        }
        else if (buah=='Kelapa') {
          hargaBuah="70000"
        }
        else if (buah=='Semangka') {
          hargaBuah="45000"
        }
        return hargaBuah;
      }
      


    </script>

  </body>
</html>
