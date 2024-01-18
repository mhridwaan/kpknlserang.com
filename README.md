# kpknlserang.com
<script src="https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js"></script>


<main id="main">
        <h1 id="title">Formulir Survei Muse ID</h1>
        <p id="description">Terima kasih telah meluangkan waktunya untuk membantu kami dalam memberikan lebih banyak anime legal berkualitas</p>

        <form name="survey-form" id="survey-form" action="">

            <div class="form-group">
                <label id="name-label" for="name">Nama</label>
                <input class="form-control" id="name" name="name" type="text" required placeholder="Masukan Nama">
            </div>

            <div class="form-group">
                <label id="email-label" for="email">
                Email
            </label>
                    <input class="form-control"
                    id="email" name="email" type="email" required placeholder="Masukan Email">
            </div>

            <div class="form-group">
                <label id="number-label" for="number">
                    Usia<span class="clue"> (opsional)</span>
                </label>
                        <input class="form-control" id="number" name="age" type="number" min="10" max="100" placeholder="Usia">
            </div>

            <div class="form-group">
                <p>Berapa waktu yang biasa anda luangkan untuk menonton anime distribusi kami?</p>
                <select id="dropdown" name="user-freetime" class="form-control" required>
                    <option disabled selected value>Pilih kisaran waktunya</option>
                    <option value="x<=5">Kurang dari 5 menit</option>
                    <option value="5<=x<=20">Diantara 5 sampai 20 menit</option>
                    <option value="x>=20">Lebih dari 20 menit</option>
                </select>
            </div>

            <div class="form-group">
                <p>Bagaimana layanan distribusi kami menurut anda?</p>
                <label>
                    <input checked name="user-experience" type="radio" class="input-radio" value="satisfied">
                    Sangat memuaskan
                </label>
                <label>
                    <input name="user-experience" type="radio" class="input-radio" value="good-enough">
                    Cukup memuaskan
                </label>
                <label>
                    <input name="user-experience" type="radio" class="input-radio" value="not-enough">
                    Kurang memuaskan
                </label>
            </div>

            <div class="form-group">
                <p>Dimana anda sering menikmati layanan kami?</p>
                <select class="form-control" name="user-platform" id="dropdown-platform">
                    <option required disabled selected value class="form-control">
                        Pilih Platform
                    </option>
                    <option value="Youtube">
                        Platform Youtube
                    </option>
                    <option value="iQiyi">Platform iQiyi</option>
                    <option value="CATCHPLAY+">Platform CATCHPLAY+</option>
                    <option value="Bilibili">Platform Bilibili</option>
                    <option value="Netflix">Platform Netflix</option>
                    <option value="AnimaxAsia">Platform Animax Asia</option>
                    <option value="AniplusAsia">Platform Aniplus Asia</option>
                </select>
            </div>

            <div class="form-group">
                <p>Apa layanan dari kami yang anda sukai?<span class="clue">(centang semua yang sesuai)</span></p>
                <label>
                    <input class="input-checkbox" type="checkbox" name="prefer1" value="animeSeries">
                    Distribusi serial anime
                </label>
                <label>
                    <input class="input-checkbox" type="checkbox" name="prefer2" value="animeFilm">
                    Distribusi film anime
                </label>
                <label>
                    <input class="input-checkbox" type="checkbox" name="prefer3" value="animeLiveAction">
                    Distribusi live action anime
                </label>
                <label>
                    <input class="input-checkbox" type="checkbox" name="prefer4" value="merchandise">
                    Distribusi merchandise
                </label>
                <label>
                    <input class="input-checkbox" type="checkbox" name="prefer5" value="asiaFilm">
                    Distribusi film asia
                </label>
                <label>
                    <input class="input-checkbox" type="checkbox" name="prefer6" value="eropaFilm">
                    Distribusi film eropa
                </label>
            </div>

            <div class="form-group">
                <p>Apakah ada komentar atau saran lainnya?</p>
                <textarea name="comment" id="comments" class="form-control input-textarea" placeholder="Masukan saran anda disini..."></textarea>
            </div>

            <div class="form-group">
                <button class="submit" id="submit" type="submit">Kirim</button>
            </div>

        </form>

        <footer id="footer" class="footer">
            <p>&copy; <a target="_blank" href="https://www.e-muse.com.sg">MUSE Communication</a></p>
        </footer>
    </main>
    

    <script>
        const scriptURL = 'https://script.google.com/macros/s/AKfycbxve3c3BbNMVx2gwl-55N40LO8pLeAHhZfACfdpi0YkZZQCIqhwMgziauepiwOmIygG/exec'
        const form = document.forms['survey-form']
      
        form.addEventListener('submit', e => {
          e.preventDefault()
          fetch(scriptURL, { method: 'POST', body: new FormData(form)})
            .then(response => {
                // tampilkan alert
                alert('Terima kasih telah mengisi formulir ini!');
                // reset form
                form.reset();
                console.log('Success!', response);
            })
            .catch(error => alert('Error!' + error.message))
        })
      </script>
