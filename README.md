# Lab2WEB
Exercise Lab 2 WEB
<h1 align="center">Hi 👋, I'm <a href="https://100rabhcsmc.github.io/Me.io/" target="blank">
Muhammad Azizul Dzikri</a> indonesia</h1>
<h3 align="center">I am a student at Pelita Bangsa University </h3>




<a target="_blank" align="center">
  <img align="right" top="500" height="300" width="400" alt="GIF" src="https://media.giphy.com/media/SWoSkN6DxTszqIKEqv/giphy.gif">
</a>

- 📫 How to reach me **azizuldzikri05@gmail.com**

<br/>
<h3 align="center" > <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30" height="30" style="margin-right: 10px;">Connect with me 🤝 </h3>




---

Credit: [dezeeonpub](https://github.com/dezeeonpub)



























Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.

+ Buat file baru dengan nama index.php dan tampil.php, file index.php digunakan sebagai tampilan utama ketika program dijalankan.
+ Kode program index.php :





=================================================================================================================================

</head>
<body>
	<h2>Form Input</h2>
	<form method="post" action="">
		Nama: <input type="text" name="nama"><br><br>
		Tanggal Lahir: <input type="date" name="tgl_lahir"><br><br>
		Pekerjaan:
		<select name="pekerjaan">
			<option value="">- Pilih Pekerjaan -</option>
			<option value="programmer">Programmer</option>
			<option value="designer">Designer</option>
			<option value="marketing">Marketing</option>
		</select><br><br>
		<input type="submit" name="submit" value="Submit">
	</form>

	<?php
		if (isset($_POST['submit'])) {
			$nama = $_POST['nama'];
			$tgl_lahir = $_POST['tgl_lahir'];
			$pekerjaan = $_POST['pekerjaan'];

			// menghitung umur berdasarkan tanggal lahir
			$umur = date_diff(date_create($tgl_lahir), date_create('today'))->y;

			// menentukan gaji berdasarkan pekerjaan
			if ($pekerjaan == 'programmer') {
				$gaji = 10000000;
			} elseif ($pekerjaan == 'designer') {
				$gaji = 8000000;
			} elseif ($pekerjaan == 'marketing') {
				$gaji = 6000000;
			}

			// menampilkan output
			echo "<h2>Output</h2>";
			echo "Nama: " . $nama . "<br>";
			echo "Tanggal Lahir: " . $tgl_lahir . "<br>";
			echo "Umur: " . $umur . " tahun<br>";
			echo "Pekerjaan: " . $pekerjaan . "<br>";
			echo "Gaji: Rp " . number_format($gaji, 0, ",", ".") . "<br>";
		}
	?>
</body>
</html>

================================================================================================================================
