# Smartendance V1

## Development Environment

- Operating System : Windows 11
- Python version : 3.12.3
- Docker Engine : Kali Linux WSLv2

## Setup & Installation

- **Clone Smartendance Repo's**:

```bash
git clone https://github.com/wahyukiddies/Smartendance-Kel2.git
```

- **Build with Docker**:

**Recommendation**: If you're using Windows, you can use `Git Bash`.

```bash
docker-compose up -d --build
```

- **Build From Source**:

```bash
# Change directory to smartendance v1
cd web/

# Install python3-venv
sudo apt install -y python3-venv
# or you can install `virtualenv` module
sudo apt install -y virtualenv

# Create new virtualenv
py -m venv .venv

# Activate virtualenv
source .venv/Scripts/activate

# Installing requirements
pip install -r requirements.txt

# Database scheme migration
# MAKE SURE YOUR MySQL DATABASE SERVER IS RUNNING !
flask db init && flask db migrate -m "Initial db migration" && flask db upgrade

# Finally, you can running the app via wsgi.py file.
py wsgi.py # Windows
python3 wsgi.py # Linux/Mac
```

## Web Preview

<div align="center">
  <b>Login Page</b><br>
  <i>Halaman masuk untuk semua user</i><br>
  <img src="https://drive.google.com/uc?id=171-gzxO71Fu5Z7NxshCjb8kevy6wnMID" width="500"/><br><br>

<b>Dashboard Admin</b><br>
<i>Menu utama untuk admin melihat data dosen dan siswa</i><br>
<img src="https://drive.google.com/uc?id=1eizodkVmMYs6G5I7BbEEoIjVPEg6L2cz" width="500"/><br><br>

<b>Lecturer Registration</b><br>
<i>Form pendaftaran dosen baru</i><br>
<img src="https://drive.google.com/uc?id=10xUIv2IgmZyG9DWsImmtdBhxLSuF8Vij" width="500"/><br><br>

<b>Student Registration</b><br>
<i>Form pendaftaran mahasiswa baru</i><br>
<img src="https://drive.google.com/uc?id=1cVfwW7fbLlYpH00mYPKF55IN2z98vZ00" width="500"/><br><br>

<b>View Course</b><br>
<i>Daftar mata kuliah yang tersedia</i><br>
<img src="https://drive.google.com/uc?id=1wJI_evTUecOyZufCy4NGzNUjq1yicBLz" width="500"/><br><br>

<b>Course Registration</b><br>
<i>Pendaftaran mata kuliah</i><br>
<img src="https://drive.google.com/uc?id=1NLlJ6hDe0wHzAJaOXOsB3os80NVN6x8d" width="500"/><br><br>

<b>Dashboard Lecturer</b><br>
<i>Menu utama dosen untuk mengelola kelas</i><br>
<img src="https://drive.google.com/uc?id=1Jk5qrj_r87_bfdbji_ERoZKZ7Qc0eQQt" width="500"/><br><br>

<b>Dashboard Student</b><br>
<i>Menu utama mahasiswa untuk melihat kehadiran dan jadwal</i><br>
<img src="https://drive.google.com/uc?id=1ZD-Cp0W5i273oTUlrO4BKdMrwN7II-jl" width="500"/>

</div>
