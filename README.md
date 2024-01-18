<div class="container">
  <header class="header">
    <h1 id="title" class="text-center">Survei Kependudukan</h1>
    <p id="description" class="description text-center">
      Sebagai warga negara Indonesia, anda wajib untuk mengisi survei di bawah ini!
    </p>
  </header>
  <form id="survey-form">
    <div class="form-group">
      <label id="name-label" for="name">Nama</label>
      <input
        type="text"
        name="namae"
        id="name"
        class="form-control"
        placeholder="Masukkan namamu"
        required
      />
    </div>
    <div class="form-group">
      <label id="email-label" for="email">NIK</label>
      <input
        type="nik"
        name="nik"
        id="nik"
        class="form-control"
        placeholder="Masukkan NIK"
        required
      />
    </div>
    <div class="form-group">
      <label id="number-label" for="number"
        >Umur<span class="clue">(optional)</span></label
      >
      <input
        type="number"
        name="umur"
        id="number"
        min="10"
        max="99"
        class="form-control"
        placeholder="Masukkan umur"
      />
    </div>
    <div class="form-group">
      <p>Agama</p>
      <select id="dropdown" name="role" class="form-control" required>
        <option disabled selected value>Pilih sesuai agamamu</option>
        <option value="islam">Islam</option>
        <option value="kristen">Kristen</option>
        <option value="katolik">Katolik</option>
        <option value="hindu">Hindu</option>
        <option value="budha">Budha</option>
      </select>
    </div>

    <div class="form-group">
      <p>Status</p>
      <label>
        <input
          name="user-recommend"
          value="definitely"
          type="radio"
          class="input-radio"
          checked
        />Belum Menikah</label
      >
      <label>
        <input
          name="user-recommend"
          value="maybe"
          type="radio"
          class="input-radio"
        />Menikah</label
      >

      <label
        ><input
          name="user-recommend"
          value="not-sure"
          type="radio"
          class="input-radio"
        />Cerai Meninggal/Cerai Hidup</label
      >
    </div>

    <div class="form-group">
      <p>Alamat</p>
      <textarea
        id="comments"
        class="input-textarea"
        name="comment"
        placeholder="Masukkan alamat"
      ></textarea>
    </div>

    <div class="form-group">
      <button type="submit" id="submit" class="submit-button">
        Submit
      </button>
    </div>
  </form>
</div>
