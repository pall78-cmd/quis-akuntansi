# quis-akuntansi
quis
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kuis Akuntansi Perusahaan Jasa</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8; /* Slightly lighter blue-gray */
            color: #334155; /* Slate-700 */
            line-height: 1.6;
        }
        .container {
            max-width: 800px;
            margin: 2rem auto;
            padding: 1.5rem;
            background-color: #ffffff;
            border-radius: 12px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        .question-card {
            background-color: #f8fafc; /* Slate-50 */
            border: 1px solid #e2e8f0; /* Slate-200 */
            border-radius: 10px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
        }
        .question-text {
            font-size: 1.125rem; /* text-lg */
            font-weight: 600; /* font-semibold */
            margin-bottom: 1rem;
            color: #1a202c; /* Gray-900 */
        }
        .option-label {
            display: flex;
            align-items: center;
            padding: 0.75rem 1rem;
            margin-bottom: 0.5rem;
            background-color: #ffffff;
            border: 1px solid #cbd5e1; /* Slate-300 */
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease-in-out;
        }
        .option-label:hover {
            background-color: #eff6ff; /* Blue-50 */
            border-color: #93c5fd; /* Blue-300 */
        }
        .option-input[type="radio"] {
            margin-right: 0.75rem;
            accent-color: #3b82f6; /* Blue-500 */
        }
        .feedback {
            margin-top: 0.75rem;
            padding: 0.5rem 1rem;
            border-radius: 8px;
            font-weight: 600;
        }
        .feedback.correct {
            background-color: #d1fae5; /* Green-100 */
            color: #065f46; /* Green-800 */
        }
        .feedback.incorrect {
            background-color: #fee2e2; /* Red-100 */
            color: #991b1b; /* Red-800 */
        }
        .submit-button, .action-button {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            background-image: linear-gradient(to right, #3b82f6, #2563eb);
            color: white;
            font-weight: 700;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.2s ease-in-out;
            box-shadow: 0 4px 10px rgba(59, 130, 246, 0.3);
            margin-top: 0.5rem;
        }
        .submit-button:hover, .action-button:hover {
            background-image: linear-gradient(to right, #2563eb, #1d4ed8);
            box-shadow: 0 6px 15px rgba(59, 130, 246, 0.4);
        }
        .score-card {
            background-color: #ecfdf5; /* Green-50 */
            border: 1px solid #a7f3d0; /* Green-200 */
            border-radius: 10px;
            padding: 2rem;
            text-align: center;
            font-size: 1.5rem;
            font-weight: 700;
            color: #065f46; /* Green-800 */
            margin-top: 2rem;
            box-shadow: 0 5px 15px rgba(16, 185, 129, 0.2);
        }
        .reset-button {
            margin-top: 1rem;
            background-color: #ef4444; /* Red-500 */
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out;
            font-weight: 600;
        }
        .reset-button:hover {
            background-color: #dc2626; /* Red-600 */
        }
        .reset-question-button { /* Style for per-question reset button */
            background-color: #6b7280; /* Gray-500 */
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out;
            font-weight: 500;
            font-size: 0.875rem; /* text-sm */
            margin-top: 1rem;
            display: block; /* Make the button appear on a new line */
            width: fit-content; /* Make width fit content */
            margin-left: auto; /* Center the button */
            margin-right: auto; /* Center the button */
        }
        .reset-question-button:hover {
            background-color: #4b5563; /* Gray-600 */
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body class="p-4">
    <div class="container">
        <h1 class="text-3xl font-bold text-center mb-2 text-gray-800">Kuis Akuntansi Perusahaan Jasa</h1>
        <p class="text-center text-gray-600 mb-6">Uji pemahaman Anda tentang Akuntansi Perusahaan Jasa!</p>

        <div id="quizSection">
            <form id="quizForm">
                <div class="question-card" id="q1">
                    <p class="question-text">1. Pada 31 Desember 2024, saldo akun Perlengkapan Kantor di neraca saldo adalah Rp1.200.000. Setelah dihitung, sisa perlengkapan yang belum terpakai adalah Rp450.000. Ayat jurnal penyesuaian yang tepat untuk mencatat beban perlengkapan adalah...</p>
                    <label class="option-label"><input type="radio" name="q1" value="a" class="option-input"> a. Beban Perlengkapan (D) Rp1.200.000; Perlengkapan Kantor (K) Rp1.200.000</label>
                    <label class="option-label"><input type="radio" name="q1" value="b" class="option-input"> b. Perlengkapan Kantor (D) Rp750.000; Beban Perlengkapan (K) Rp750.000</label>
                    <label class="option-label"><input type="radio" name="q1" value="c" class="option-input"> c. Beban Perlengkapan (D) Rp750.000; Perlengkapan Kantor (K) Rp750.000</label>
                    <label class="option-label"><input type="radio" name="q1" value="d" class="option-input"> d. Beban Perlengkapan (D) Rp450.000; Perlengkapan Kantor (K) Rp450.000</label>
                    <label class="option-label"><input type="radio" name="q1" value="e" class="option-input"> e. Perlengkapan Kantor (D) Rp450.000; Beban Perlengkapan (K) Rp450.000</label>
                    <div class="feedback" id="feedback-q1"></div>
                    <button type="button" class="reset-question-button" data-question-id="q1">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q2">
                    <p class="question-text">2. Sebuah perusahaan jasa membeli peralatan pada 1 Januari 2024 seharga Rp50.000.000. Peralatan ini diperkirakan memiliki masa manfaat 10 tahun tanpa nilai residu. Dengan menggunakan metode garis lurus, jurnal penyesuaian untuk beban penyusutan pada 31 Desember 2024 adalah...</p>
                    <label class="option-label"><input type="radio" name="q2" value="a" class="option-input"> a. Beban Penyusutan Peralatan (D) Rp5.000.000; Peralatan (K) Rp5.000.000</label>
                    <label class="option-label"><input type="radio" name="q2" value="b" class="option-input"> b. Beban Penyusutan Peralatan (D) Rp5.000.000; Akumulasi Penyusutan Peralatan (K) Rp5.000.000</label>
                    <label class="option-label"><input type="radio" name="q2" value="c" class="option-input"> c. Peralatan (D) Rp5.000.000; Beban Penyusutan Peralatan (K) Rp5.000.000</label>
                    <label class="option-label"><input type="radio" name="q2" value="d" class="option-input"> d. Akumulasi Penyusutan Peralatan (D) Rp5.000.000; Beban Penyusutan Peralatan (K) Rp5.000.000</label>
                    <label class="option-label"><input type="radio" name="q2" value="e" class="option-input"> e. Beban Peralatan (D) Rp5.000.000; Kas (K) Rp5.000.000</label>
                    <div class="feedback" id="feedback-q2"></div>
                    <button type="button" class="reset-question-button" data-question-id="q2">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q3">
                    <p class="question-text">3. Pada 1 November 2024, sebuah firma hukum menerima uang muka sebesar Rp6.000.000 dari klien untuk jasa konsultasi yang akan diberikan selama 3 bulan. Firma hukum mencatatnya sebagai Pendapatan Jasa Diterima di Muka. Pada 31 Desember 2024, jurnal penyesuaian yang harus dibuat adalah...</p>
                    <label class="option-label"><input type="radio" name="q3" value="a" class="option-input"> a. Kas (D) Rp6.000.000; Pendapatan Jasa Diterima di Muka (K) Rp6.000.000</label>
                    <label class="option-label"><input type="radio" name="q3" value="b" class="option-input"> b. Pendapatan Jasa Diterima di Muka (D) Rp6.000.000; Pendapatan Jasa (K) Rp6.000.000</label>
                    <label class="option-label"><input type="radio" name="q3" value="c" class="option-input"> c. Pendapatan Jasa Diterima di Muka (D) Rp4.000.000; Pendapatan Jasa (K) Rp4.000.000</label>
                    <label class="option-label"><input type="radio" name="q3" value="d" class="option-input"> d. Pendapatan Jasa (D) Rp4.000.000; Pendapatan Jasa Diterima di Muka (K) Rp4.000.000</label>
                    <label class="option-label"><input type="radio" name="q3" value="e" class="option-input"> e. Pendapatan Jasa Diterima di Muka (D) Rp2.000.000; Pendapatan Jasa (K) Rp2.000.000</label>
                    <div class="feedback" id="feedback-q3"></div>
                    <button type="button" class="reset-question-button" data-question-id="q3">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q4">
                    <p class="question-text">4. Sebuah perusahaan menyewa gedung dengan membayar di muka pada 1 September 2024 sebesar Rp12.000.000 untuk 1 tahun. Jika pada saat pembayaran dicatat sebagai Beban Sewa, maka jurnal penyesuaian pada 31 Desember 2024 adalah...</p>
                    <label class="option-label"><input type="radio" name="q4" value="a" class="option-input"> a. Beban Sewa (D) Rp12.000.000; Kas (K) Rp12.000.000</label>
                    <label class="option-label"><input type="radio" name="q4" value="b" class="option-input"> b. Sewa Dibayar di Muka (D) Rp8.000.000; Beban Sewa (K) Rp8.000.000</label>
                    <label class="option-label"><input type="radio" name="q4" value="c" class="option-input"> c. Beban Sewa (D) Rp8.000.000; Sewa Dibayar di Muka (K) Rp8.000.000</label>
                    <label class="option-label"><input type="radio" name="q4" value="d" class="option-input"> d. Sewa Dibayar di Muka (D) Rp4.000.000; Beban Sewa (K) Rp4.000.000</label>
                    <label class="option-label"><input type="radio" name="q4" value="e" class="option-input"> e. Beban Sewa (D) Rp4.000.000; Sewa Dibayar di Muka (K) Rp4.000.000</label>
                    <div class="feedback" id="feedback-q4"></div>
                    <button type="button" class="reset-question-button" data-question-id="q4">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q5">
                    <p class="question-text">5. Gaji karyawan yang belum dibayar hingga 31 Desember 2024 adalah Rp7.500.000. Jurnal penyesuaian yang diperlukan untuk mencatat utang gaji adalah...</p>
                    <label class="option-label"><input type="radio" name="q5" value="a" class="option-input"> a. Kas (D) Rp7.500.000; Beban Gaji (K) Rp7.500.000</label>
                    <label class="option-label"><input type="radio" name="q5" value="b" class="option-input"> b. Utang Gaji (D) Rp7.500.000; Beban Gaji (K) Rp7.500.000</label>
                    <label class="option-label"><input type="radio" name="q5" value="c" class="option-input"> c. Beban Gaji (D) Rp7.500.000; Utang Gaji (K) Rp7.500.000</label>
                    <label class="option-label"><input type="radio" name="q5" value="d" class="option-input"> d. Beban Gaji (D) Rp7.500.000; Kas (K) Rp7.500.000</label>
                    <label class="option-label"><input type="radio" name="q5" value="e" class="option-input"> e. Tidak ada jurnal penyesuaian yang diperlukan</label>
                    <div class="feedback" id="feedback-q5"></div>
                    <button type="button" class="reset-question-button" data-question-id="q5">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q6">
                    <p class="question-text">6. Pendapatan jasa yang telah diberikan tetapi belum ditagih kepada pelanggan hingga 31 Desember 2024 berjumlah Rp2.500.000. Ayat jurnal penyesuaian yang benar adalah...</p>
                    <label class="option-label"><input type="radio" name="q6" value="a" class="option-input"> a. Kas (D) Rp2.500.000; Pendapatan Jasa (K) Rp2.500.000</label>
                    <label class="option-label"><input type="radio" name="q6" value="b" class="option-input"> b. Pendapatan Jasa (D) Rp2.500.000; Piutang Usaha (K) Rp2.500.000</label>
                    <label class="option-label"><input type="radio" name="q6" value="c" class="option-input"> c. Piutang Usaha (D) Rp2.500.000; Pendapatan Jasa (K) Rp2.500.000</label>
                    <label class="option-label"><input type="radio" name="q6" value="d" class="option-input"> d. Pendapatan Diterima di Muka (D) Rp2.500.000; Pendapatan Jasa (K) Rp2.500.000</label>
                    <label class="option-label"><input type="radio" name="q6" value="e" class="option-input"> e. Beban Jasa (D) Rp2.500.000; Utang Usaha (K) Rp2.500.000</label>
                    <div class="feedback" id="feedback-q6"></div>
                    <button type="button" class="reset-question-button" data-question-id="q6">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q7">
                    <p class="question-text">7. Pada 1 Maret 2024, perusahaan membayar premi asuransi untuk 1 tahun sebesar Rp2.400.000. Saat pembayaran, dicatat ke akun Asuransi Dibayar di Muka. Jurnal penyesuaian yang diperlukan pada 31 Desember 2024 adalah...</p>
                    <label class="option-label"><input type="radio" name="q7" value="a" class="option-input"> a. Beban Asuransi (D) Rp2.400.000; Asuransi Dibayar di Muka (K) Rp2.400.000</label>
                    <label class="option-label"><input type="radio" name="q7" value="b" class="option-input"> b. Asuransi Dibayar di Muka (D) Rp2.000.000; Beban Asuransi (K) Rp2.000.000</label>
                    <label class="option-label"><input type="radio" name="q7" value="c" class="option-input"> c. Beban Asuransi (D) Rp2.000.000; Asuransi Dibayar di Muka (K) Rp2.000.000</label>
                    <label class="option-label"><input type="radio" name="q7" value="d" class="option-input"> d. Asuransi Dibayar di Muka (D) Rp400.000; Beban Asuransi (K) Rp400.000</label>
                    <label class="option-label"><input type="radio" name="q7" value="e" class="option-input"> e. Beban Asuransi (D) Rp400.000; Asuransi Dibayar di Muka (K) Rp400.000</label>
                    <div class="feedback" id="feedback-q7"></div>
                    <button type="button" class="reset-question-button" data-question-id="q7">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q8">
                    <p class="question-text">8. Manakah dari akun berikut yang akan selalu muncul di sisi Liabilitas pada neraca?</p>
                    <label class="option-label"><input type="radio" name="q8" value="a" class="option-input"> a. Kas</label>
                    <label class="option-label"><input type="radio" name="q8" value="b" class="option-input"> b. Modal</label>
                    <label class="option-label"><input type="radio" name="q8" value="c" class="option-input"> c. Utang Usaha</label>
                    <label class="option-label"><input type="radio" name="q8" value="d" class="option-input"> d. Pendapatan Jasa</label>
                    <label class="option-label"><input type="radio" name="q8" value="e" class="option-input"> e. Beban Gaji</label>
                    <div class="feedback" id="feedback-q8"></div>
                    <button type="button" class="reset-question-button" data-question-id="q8">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q9">
                    <p class="question-text">9. Akun Pendapatan Jasa Diterima di Muka pada neraca termasuk dalam kategori...</p>
                    <label class="option-label"><input type="radio" name="q9" value="a" class="option-input"> a. Aset Lancar</label>
                    <label class="option-label"><input type="radio" name="q9" value="b" class="option-input"> b. Aset Tidak Lancar</label>
                    <label class="option-label"><input type="radio" name="q9" value="c" class="option-input"> c. Liabilitas Jangka Pendek</label>
                    <label class="option-label"><input type="radio" name="q9" value="d" class="option-input"> d. Liabilitas Jangka Panjang</label>
                    <label class="option-label"><input type="radio" name="q9" value="e" class="option-input"> e. Ekuitas</label>
                    <div class="feedback" id="feedback-q9"></div>
                    <button type="button" class="reset-question-button" data-question-id="q9">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q10">
                    <p class="question-text">10. Berikut adalah sebagian data keuangan sebuah perusahaan jasa per 31 Desember 2024: <br><br>Kas: Rp20.000.000 <br>Piutang Usaha: Rp12.000.000 <br>Perlengkapan Kantor: Rp3.000.000 <br>Peralatan: Rp60.000.000 <br>Akumulasi Penyusutan Peralatan: Rp10.000.000 <br>Utang Usaha: Rp8.000.000 <br>Utang Gaji: Rp5.000.000 <br>Modal Tn. Adi: Rp72.000.000 <br><br>Berapakah total aset lancar perusahaan jasa tersebut?</p>
                    <label class="option-label"><input type="radio" name="q10" value="a" class="option-input"> a. Rp63.000.000</label>
                    <label class="option-label"><input type="radio" name="q10" value="b" class="option-input"> b. Rp35.000.000</label>
                    <label class="option-label"><input type="radio" name="q10" value="c" class="option-input"> c. Rp75.000.000</label>
                    <label class="option-label"><input type="radio" name="q10" value="d" class="option-input"> d. Rp32.000.000</label>
                    <label class="option-label"><input type="radio" name="q10" value="e" class="option-input"> e. Rp50.000.000</label>
                    <div class="feedback" id="feedback-q10"></div>
                    <button type="button" class="reset-question-button" data-question-id="q10">Reset Jawaban</button>
                </div>
                 <div class="question-card" id="q11">
                    <p class="question-text">11. Berdasarkan data soal nomor 10, berapakah nilai buku Peralatan pada neraca?</p>
                    <label class="option-label"><input type="radio" name="q11" value="a" class="option-input"> a. Rp60.000.000</label>
                    <label class="option-label"><input type="radio" name="q11" value="b" class="option-input"> b. Rp10.000.000</label>
                    <label class="option-label"><input type="radio" name="q11" value="c" class="option-input"> c. Rp70.000.000</label>
                    <label class="option-label"><input type="radio" name="q11" value="d" class="option-input"> d. Rp50.000.000</label>
                    <label class="option-label"><input type="radio" name="q11" value="e" class="option-input"> e. Rp0</label>
                    <div class="feedback" id="feedback-q11"></div>
                    <button type="button" class="reset-question-button" data-question-id="q11">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q12">
                    <p class="question-text">12. Dalam neraca, akun Utang Bank Jangka Panjang menunjukkan...</p>
                    <label class="option-label"><input type="radio" name="q12" value="a" class="option-input"> a. Aset yang dimiliki perusahaan</label>
                    <label class="option-label"><input type="radio" name="q12" value="b" class="option-input"> b. Pendapatan yang akan diterima</label>
                    <label class="option-label"><input type="radio" name="q12" value="c" class="option-input"> c. Kewajiban perusahaan yang jatuh temponya lebih dari satu tahun</label>
                    <label class="option-label"><input type="radio" name="q12" value="d" class="option-input"> d. Beban yang harus dibayar segera</label>
                    <label class="option-label"><input type="radio" name="q12" value="e" class="option-input"> e. Modal yang disetor oleh pemilik</label>
                    <div class="feedback" id="feedback-q12"></div>
                    <button type="button" class="reset-question-button" data-question-id="q12">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q13">
                    <p class="question-text">13. Jika suatu perusahaan mencatat sewa dibayar di muka sebagai aset, maka pada akhir periode, saat sebagian sewa sudah menjadi beban, akun yang akan dikredit dalam jurnal penyesuaian adalah...</p>
                    <label class="option-label"><input type="radio" name="q13" value="a" class="option-input"> a. Kas</label>
                    <label class="option-label"><input type="radio" name="q13" value="b" class="option-input"> b. Beban Sewa</label>
                    <label class="option-label"><input type="radio" name="q13" value="c" class="option-input"> c. Sewa Dibayar di Muka</label>
                    <label class="option-label"><input type="radio" name="q13" value="d" class="option-input"> d. Pendapatan Sewa</label>
                    <label class="option-label"><input type="radio" name="q13" value="e" class="option-input"> e. Piutang Sewa</label>
                    <div class="feedback" id="feedback-q13"></div>
                    <button type="button" class="reset-question-button" data-question-id="q13">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q14">
                    <p class="question-text">14. Saldo akun pendapatan jasa pada neraca saldo adalah Rp15.000.000. Namun, ada jasa yang telah diselesaikan tetapi belum ditagih sebesar Rp3.000.000. Jurnal penyesuaian yang akan mempengaruhi nilai pendapatan jasa pada laporan laba rugi adalah...</p>
                    <label class="option-label"><input type="radio" name="q14" value="a" class="option-input"> a. Pendapatan Jasa (D) Rp3.000.000; Piutang Usaha (K) Rp3.000.000</label>
                    <label class="option-label"><input type="radio" name="q14" value="b" class="option-input"> b. Piutang Usaha (D) Rp3.000.000; Pendapatan Jasa (K) Rp3.000.000</label>
                    <label class="option-label"><input type="radio" name="q14" value="c" class="option-input"> c. Kas (D) Rp3.000.000; Pendapatan Jasa (K) Rp3.000.000</label>
                    <label class="option-label"><input type="radio" name="q14" value="d" class="option-input"> d. Pendapatan Diterima di Muka (D) Rp3.000.000; Pendapatan Jasa (K) Rp3.000.000</label>
                    <label class="option-label"><input type="radio" name="q14" value="e" class="option-input"> e. Tidak ada jurnal penyesuaian yang diperlukan</label>
                    <div class="feedback" id="feedback-q14"></div>
                    <button type="button" class="reset-question-button" data-question-id="q14">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q15">
                    <p class="question-text">15. Neraca menyajikan informasi yang sangat penting bagi pengambilan keputusan karena menunjukkan...</p>
                    <label class="option-label"><input type="radio" name="q15" value="a" class="option-input"> a. Laba atau rugi bersih perusahaan selama satu tahun.</label>
                    <label class="option-label"><input type="radio" name="q15" value="b" class="option-input"> b. Arus kas masuk dan keluar dari aktivitas operasi, investasi, dan pendanaan.</label>
                    <label class="option-label"><input type="radio" name="q15" value="c" class="option-input"> c. Posisi keuangan (aset, liabilitas, dan ekuitas) perusahaan pada suatu tanggal tertentu.</label>
                    <label class="option-label"><input type="radio" name="q15" value="d" class="option-input"> d. Perubahan dalam modal pemilik selama periode berjalan.</label>
                    <label class="option-label"><input type="radio" name="q15" value="e" class="option-input"> e. Rincian semua transaksi yang terjadi selama periode akuntansi.</label>
                    <div class="feedback" id="feedback-q15"></div>
                    <button type="button" class="reset-question-button" data-question-id="q15">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q16">
                    <p class="question-text">16. Setelah semua jurnal penyesuaian diposting ke buku besar, tahapan selanjutnya dalam siklus akuntansi untuk menyusun laporan keuangan adalah...</p>
                    <label class="option-label"><input type="radio" name="q16" value="a" class="option-input"> a. Menyusun jurnal penutup.</label>
                    <label class="option-label"><input type="radio" name="q16" value="b" class="option-input"> b. Membuat neraca saldo setelah penyesuaian.</label>
                    <label class="option-label"><input type="radio" name="q16" value="c" class="option-input"> c. Membuat jurnal pembalik.</label>
                    <label class="option-label"><input type="radio" name="q16" value="d" class="option-input"> d. Menyusun laporan arus kas.</label>
                    <label class="option-label"><input type="radio" name="q16" value="e" class="option-input"> e. Menyusun neraca saldo sebelum penyesuaian.</label>
                    <div class="feedback" id="feedback-q16"></div>
                    <button type="button" class="reset-question-button" data-question-id="q16">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q17">
                    <p class="question-text">17. Jika saldo Beban Gaji di neraca saldo adalah Rp10.000.000 dan terdapat gaji yang masih harus dibayar sebesar Rp2.000.000, maka setelah penyesuaian, nilai Beban Gaji yang akan muncul di laporan laba rugi adalah...</p>
                    <label class="option-label"><input type="radio" name="q17" value="a" class="option-input"> a. Rp10.000.000</label>
                    <label class="option-label"><input type="radio" name="q17" value="b" class="option-input"> b. Rp8.000.000</label>
                    <label class="option-label"><input type="radio" name="q17" value="c" class="option-input"> c. Rp12.000.000</label>
                    <label class="option-label"><input type="radio" name="q17" value="d" class="option-input"> d. Rp2.000.000</label>
                    <label class="option-label"><input type="radio" name="q17" value="e" class="option-input"> e. Rp0</label>
                    <div class="feedback" id="feedback-q17"></div>
                    <button type="button" class="reset-question-button" data-question-id="q17">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q18">
                    <p class="question-text">18. Sebuah perusahaan jasa menerima uang muka dari pelanggan sebesar Rp5.000.000. Pencatatan awal dilakukan dengan mendebet Kas dan mengkredit Pendapatan Jasa Diterima di Muka. Ayat jurnal penyesuaian yang tepat jika pada akhir periode jasa senilai Rp2.000.000 telah diselesaikan adalah...</p>
                    <label class="option-label"><input type="radio" name="q18" value="a" class="option-input"> a. Kas (D) Rp2.000.000; Pendapatan Jasa (K) Rp2.000.000</label>
                    <label class="option-label"><input type="radio" name="q18" value="b" class="option-input"> b. Pendapatan Jasa Diterima di Muka (D) Rp3.000.000; Pendapatan Jasa (K) Rp3.000.000</label>
                    <label class="option-label"><input type="radio" name="q18" value="c" class="option-input"> c. Pendapatan Jasa (D) Rp2.000.000; Pendapatan Jasa Diterima di Muka (K) Rp2.000.000</label>
                    <label class="option-label"><input type="radio" name="q18" value="d" class="option-input"> d. Pendapatan Jasa Diterima di Muka (D) Rp2.000.000; Pendapatan Jasa (K) Rp2.000.000</label>
                    <label class="option-label"><input type="radio" name="q18" value="e" class="option-input"> e. Piutang Usaha (D) Rp2.000.000; Pendapatan Jasa (K) Rp2.000.000</label>
                    <div class="feedback" id="feedback-q18"></div>
                    <button type="button" class="reset-question-button" data-question-id="q18">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q19">
                    <p class="question-text">19. Manakah pernyataan berikut yang paling tepat mengenai tujuan utama penyusunan jurnal penyesuaian?</p>
                    <label class="option-label"><input type="radio" name="q19" value="a" class="option-input"> a. Untuk mencatat penerimaan dan pengeluaran kas harian.</label>
                    <label class="option-label"><input type="radio" name="q19" value="b" class="option-input"> b. Untuk menutup akun-akun temporer pada akhir periode.</label>
                    <label class="option-label"><input type="radio" name="q19" value="c" class="option-input"> c. Untuk memastikan bahwa pendapatan dan beban diakui pada periode akuntansi yang benar, terlepas dari arus kasnya.</label>
                    <label class="option-label"><input type="radio" name="q19" value="d" class="option-input"> d. Untuk mengidentifikasi kesalahan pencatatan transaksi yang telah lalu.</label>
                    <label class="option-label"><input type="radio" name="q19" value="e" class="option-input"> e. Untuk mencatat transaksi pembelian aset jangka panjang.</label>
                    <div class="feedback" id="feedback-q19"></div>
                    <button type="button" class="reset-question-button" data-question-id="q19">Reset Jawaban</button>
                </div>
                <div class="question-card" id="q20">
                    <p class="question-text">20. Jika total aset suatu perusahaan jasa adalah Rp150.000.000 dan total ekuitas pemilik adalah Rp90.000.000, berapakah total liabilitasnya?</p>
                    <label class="option-label"><input type="radio" name="q20" value="a" class="option-input"> a. Rp60.000.000</label>
                    <label class="option-label"><input type="radio" name="q20" value="b" class="option-input"> b. Rp240.000.000</label>
                    <label class="option-label"><input type="radio" name="q20" value="c" class="option-input"> c. Rp90.000.000</label>
                    <label class="option-label"><input type="radio" name="q20" value="d" class="option-input"> d. Rp150.000.000</label>
                    <label class="option-label"><input type="radio" name="q20" value="e" class="option-input"> e. Rp0</label>
                    <div class="feedback" id="feedback-q20"></div>
                    <button type="button" class="reset-question-button" data-question-id="q20">Reset Jawaban</button>
                </div>
                <button type="submit" class="submit-button w-full">Periksa Jawaban</button>
            </form>
        </div>

        <div id="scoreDisplaySection" class="score-card hidden">
            <p>Skor Anda: <span id="score">0</span> dari <span id="totalQuestionsDisplay">20</span></p>
        </div>
        
        <button id="resetQuizButton" class="reset-button w-full mt-6 hidden">Ulangi Kuis</button>
    </div>

    <script type="module">
        // Global variables for the quiz application
        let currentScore = 0;
        const totalQuestions = 20;

        // Correct answers for each question
        const correctAnswers = {
            q1: 'c', q2: 'b', q3: 'c', q4: 'b', q5: 'c',
            q6: 'c', q7: 'c', q8: 'c', q9: 'c', q10: 'b',
            q11: 'd', q12: 'c', q13: 'c', q14: 'b', q15: 'c',
            q16: 'b', q17: 'c', q18: 'd', q19: 'c', q20: 'a'
        };

        // DOM elements
        const quizForm = document.getElementById('quizForm');
        const scoreDisplaySection = document.getElementById('scoreDisplaySection');
        const scoreDisplay = document.getElementById('score');
        const totalQuestionsDisplay = document.getElementById('totalQuestionsDisplay');
        const resetQuizButton = document.getElementById('resetQuizButton');

        /**
         * Resets the selected answer and feedback for a specific question.
         * @param {string} questionId - The ID of the question to reset (e.g., 'q1').
         */
        function resetQuestion(questionId) {
            // Uncheck all radio buttons for the given question
            const radioButtons = document.querySelectorAll(`input[name="${questionId}"]`);
            radioButtons.forEach(radio => {
                radio.checked = false;
                radio.disabled = false; // Re-enable radio buttons
            });

            // Clear feedback message and styling
            const feedbackElement = document.getElementById(`feedback-${questionId}`);
            if (feedbackElement) {
                feedbackElement.textContent = '';
                feedbackElement.classList.remove('correct', 'incorrect');
            }
            
            // If the quiz was already checked, re-hide the score display
            // and re-show the main submit button to allow re-checking.
            // This ensures consistency if a user resets a question after seeing their score.
            if (!scoreDisplaySection.classList.contains('hidden')) {
                scoreDisplaySection.classList.add('hidden');
            }
            if (quizForm.querySelector('.submit-button').classList.contains('hidden')) {
                quizForm.querySelector('.submit-button').classList.remove('hidden');
            }
            resetQuizButton.classList.add('hidden'); // Hide the main reset button if individual question is reset
        }

        /**
         * Checks all answers, calculates the score, and displays feedback.
         */
        function checkAnswers() {
            currentScore = 0; // Reset score before recalculating
            for (let i = 1; i <= totalQuestions; i++) {
                const questionName = `q${i}`;
                const selectedOption = document.querySelector(`input[name="${questionName}"]:checked`);
                const feedbackElement = document.getElementById(`feedback-${questionName}`);
                
                // Clear previous feedback
                feedbackElement.textContent = '';
                feedbackElement.classList.remove('correct', 'incorrect');

                if (selectedOption) {
                    if (selectedOption.value === correctAnswers[questionName]) {
                        currentScore++;
                        feedbackElement.textContent = 'Jawaban Benar!';
                        feedbackElement.classList.add('correct');
                    } else {
                        feedbackElement.textContent = `Jawaban Salah. Benar: ${correctAnswers[questionName].toUpperCase()}.`;
                        feedbackElement.classList.add('incorrect');
                    }
                    // Disable radio buttons for this question after checking
                    document.querySelectorAll(`input[name="${questionName}"]`).forEach(radio => radio.disabled = true);
                } else {
                    feedbackElement.textContent = 'Anda belum memilih jawaban.';
                    feedbackElement.classList.add('incorrect');
                    // Ensure radio buttons are disabled even if not answered
                    document.querySelectorAll(`input[name="${questionName}"]`).forEach(radio => radio.disabled = true);
                }
            }

            // Display final score
            scoreDisplay.textContent = currentScore;
            totalQuestionsDisplay.textContent = totalQuestions;
            scoreDisplaySection.classList.remove('hidden');
            quizForm.querySelector('.submit-button').classList.add('hidden'); // Hide the main check button
            
            resetQuizButton.classList.remove('hidden'); // Show the main reset quiz button
        }

        /**
         * Resets the entire quiz, clearing all selections and feedback.
         */
        function resetQuiz() {
            quizForm.reset(); // Reset all form inputs (unchecks all radio buttons)
            currentScore = 0; // Reset score

            for (let i = 1; i <= totalQuestions; i++) {
                const questionName = `q${i}`;
                const feedbackElement = document.getElementById(`feedback-${questionName}`);
                feedbackElement.textContent = ''; // Clear feedback text
                feedbackElement.classList.remove('correct', 'incorrect'); // Remove feedback styling
                // Re-enable all radio buttons
                document.querySelectorAll(`input[name="${questionName}"]`).forEach(radio => radio.disabled = false);
            }

            scoreDisplaySection.classList.add('hidden'); // Hide the score display
            
            quizForm.querySelector('.submit-button').classList.remove('hidden'); // Show the main check button again
            resetQuizButton.classList.add('hidden'); // Hide the main reset quiz button
        }

        // Event Listeners
        // Listen for the main quiz form submission
        quizForm.addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent default form submission behavior
            checkAnswers(); // Run the answer checking function
        });

        // Listen for the main "Ulangi Kuis" button click
        resetQuizButton.addEventListener('click', resetQuiz);

        // Add event listeners for each individual "Reset Jawaban" button
        document.querySelectorAll('.reset-question-button').forEach(button => {
            button.addEventListener('click', function() {
                const questionId = this.dataset.questionId; // Get the question ID from data-attribute
                resetQuestion(questionId); // Call reset function for that specific question
            });
        });

        // Initialize the quiz when the page loads
        document.addEventListener('DOMContentLoaded', resetQuiz);

    </script>
</body>
</html>

