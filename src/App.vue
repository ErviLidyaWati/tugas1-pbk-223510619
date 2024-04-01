
<template>
  
  <div class="portfolio">
        <div class="left-column">
      <div class="personal-info">
        <div class="profile-picture">
          <img src="c:\Users\HP\OneDrive\Pictures\IMG_20220714_110248-removebg.png" alt="Profile Picture" />
        </div>
        <div class="info">
          <h1>{{ nama }}</h1>
          <div class="icon-text">
            <i class="fas fa-envelope"></i>
            <span>{{ email }}</span>
          </div>

          <div class="icon-text">
            <i class="fas fa-phone"></i>
            <span>{{ phone }}</span>
          </div>

          <hr class="divider" />
          <h3>Keterampilan</h3>
          <ul class="skills">
            <li v-for="(skill, index) in skills" :key="index">
              <i class="fas fa-check"></i>
              {{ skill }}
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="right-column">
      <div class="section">
        <h2 class="section-title" >Pendidikan</h2>
        <div class="timeline">
          <div v-for="(education, index) in educationList" :key="index" class="event">
            <div class="event-title">{{ education.title }}</div>
            <div class="event-subtitle">{{ education.subtitle }}</div>
            <div class="event-date">{{ education.date }}</div>
          </div>
        </div>
      </div>

      <div class="section">
        <h2 class="section-title">Prestasi Akademik</h2>
        <div class="timeline">
          <div v-for="(experience, index) in experienceList" :key="index" class="event">
            <div class="event-title">{{ experience.title }}</div>
            <div class="event-subtitle">{{ experience.subtitle }}</div>
            <div class="event-date">{{ experience.date }}</div>
          </div>
        </div>
      </div>

      <div class="section">
        <h2 class="section-title">Proyek Pribadi</h2>
        <div class="projects">
          <div v-for="(project, index) in projectsList" :key="index" class="project">
            <div class="project-title">{{ project.title }}</div>
            <div class="project-description">{{ project.description }}</div>
            <div class="project-date">{{ project.date }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      nama: 'Ervi Lidya Wati',
      email: 'ervilidyawati@student.uir.ac.id',
      phone: '+62 812 4567 890',
      skills: ['HTML', 'CSS', 'JavaScript', 'Vue.js', 'Phyton', 'Git'],
      educationList: [
        {
          title: 'S1 Teknik Informatika',
          subtitle: 'Universitas Islam Riau, Kota Pekanbaru',
          date: '2022 - Sekarang',
        },
        {
          title: 'SMA Negeri 1 Kampar Kiri Tengah',
          subtitle: 'Jurusan IPA',
          date: '2019 - 2021',
        },
      ],
      experienceList: [
        {
          title: 'Desain Flayer',
          subtitle: 'Universitas Islma Riau, Kota Pekanbaru',
          date: '2023',
        },
        {
          title: 'Karya Tulis Ilmiah',
          subtitle: 'Universitas Islma Riau, Kota Pekanbaru',
          date: '2023',
        },
      ],
      projectsList: [
        {
          title: 'Business Plan',
          description: 'Perancangan Bisnis Makanan ',
          date: '2023',
        },
        {
          title: 'Website Portfolio Pribadi',
          description: 'Desain dan pengembangan website portfolio dengan Vue.js',
          date: '2024',
        },
        {
          title: 'Aplikasi Mobile Kesehatan Hewan',
          description: 'Perancangan aplikasi mobile untuk Kesehatan Hewan',
          date: '2023',
        },
      ],
    };
  },
};
</script>

<style scoped>
.portfolio {
  display: flex;
  width:1400PX;
  color: #0d0d0d;
  margin: 0 auto;
  font-family: helvetica, sans-serif;
}

.left-column {
  flex: 1 ;
  background-color: #979494;
  padding: 50px;
  border-right: 2px solid #ccc;
}

.right-column {
  flex: 1.5;
  background-color: #ecc2c2;
  padding: 50px;
}

.profile-picture img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 30px;
}

.info h1 {
  font-size: 24px;
  margin: 0 0 10px 0;
}

.icon-text {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}

.icon-text i {
  margin-right: 10px;
}

.skills {
  margin-top: 20px;
  list-style: none;
  padding: 0;
}

.skills li {
  display: flex;
  align-items: center;
  margin-bottom: 5px;
}

.skills li i {
  margin-right: 10px;
}

.right-column .section {
  margin-bottom: 40px;
}

.section-title {
  font-size: 24px;
  margin-bottom: 20px;
}

.timeline .event {
  position: relative;
  padding-left: 20px;
  margin-bottom: 20px;
}

.timeline .event:before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 4px;
  background-color: grey;
}

.timeline .event-title {
  font-size: 18px;
  font-weight: bold;
}

.timeline .event-subtitle {
  font-size: 16px;
  color: black;
}

.timeline .event-date {
  font-size: 14px;
  color: #050505;
}

.projects .project {
  margin-bottom: 20px;
}

.project-title {
  font-size: 18px;
  color: grey;
  font-weight: bold;
  margin-bottom: 5px;
}

.project-description {
  font-size: 16px;
  color: #1f1c1c;
}

.project-date {
  font-size: 14px;
  color: #0a0a0a;
}
</style>
