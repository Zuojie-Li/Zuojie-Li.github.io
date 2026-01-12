---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Basic
======
* Born: December 1996​
* party: Member of the Communist Party of China
* Workplace: Postdoc. Key Laboratory of Radiopharmaceuticals / Beam Technology of the Ministry of Education, Beijing Normal University

Education
======
* Ph.D in BeiJing Normal University, 2025
* M.S. in LiaoCheng Univeristy,  2022
* B.S. in LiaoCheng University, 2019

Work experience
======
* China Resources Snow Breweries，2017.10-2017.11
 
* Hengrui Pharmaceutical​，2018.12-2019.01
 
* NHU Pharmaceutical，2019.02-2019.07
  
Skills
======
* Computer-Aided Drug Design
  * Homology Modeling 
  * Design Optimization for Structures
  * Molecular Dynamics Simulation

* ​Antineoplastic Drugs​​ 
  * Target screening
  * Bioactivity Assessment
  * Mechanistic Study

* Radiopharmaceutical Drugs
  * PET
  * SPECT

Publications (1st. author)
======
* J Med Chem, 2025, ASAP.
* J Med Chem, 2025, 68(21), 23620-23631.
* J Med Chem, 2024, 67(24), 21644-21670.
* J Med Chem, 2024, 67(23), 21617-21628.
* J Med Chem, 2021, 64(24), 17920-17935.
* Mol Pharm, 2024, 21(10), 5305-5314.
* Mini Rew Med Chem, 2025, 25(17), 1321-1333.
* Dalton Trans, 2022, 51(33), 12604-12619.
* Dalton Trans, 2021, 50(1), 362-375.
* Monatsh Chem, 2020, 151(3), 353-367.
* J Liaocheng Univ, 2020, 33(5), 97-103. 

Awards
======
* The First-Class Award for Excellent Graduate Research at Liaocheng University
* The First Prize for Poster Presentation at the 4th Graduate Academic Conference of the College of Chemistry, Beijing Normal University
* The Excellent Poster Award at the 17th National Academic Conference on Radiopharmaceuticals and Labeled Compounds，Xian
* Atomic High-Tech Scholarship for Ph.D. Candidates

About Me
======
<!-- 滚动相框组件 - 紧凑版 -->
<style>
.photo-gallery-container {
  background: white;
  border-radius: 6px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.06);
  padding: 10px;
  margin: 8px 0;
  border-top: 2px solid #3498db;
}
.gallery-title {
  font-size: 1.1rem;
  font-weight: bold;
  background: linear-gradient(90deg, 
      #ff6b6b,  /* 柔和红 */
      #ffa726,  /* 柔和橙 */
      #ffd93d,  /* 柔和黄 */
      #4cd964,  /* 柔和绿 */
      #5ac8fa,  /* 柔和蓝 */
      #af52de,  /* 柔和紫 */
      #ff6b6b   /* 回到柔和红 */
  );
  background-size: 200% 100%;
  animation: softRainbow 10s ease-in-out infinite;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-align: center;
  font-family: 'Helvetica Neue', sans-serif;
  text-shadow: 0 0 12px rgba(255, 255, 255, 0.3);
  margin: 0 0 10px 0;
  padding: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}
@keyframes softRainbow {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

/* 主要修改：相框高度从320px减小到260px */
.photo-frame {
  height: 260px; /* 减小了60px */
  background: #f8f9fa;
  border-radius: 5px;
  padding: 5px;
  position: relative;
  overflow: hidden;
}
.photo-frame::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, #3498db, #2ecc71, #e74c3c);
}
.scrolling-photos {
  display: flex;
  height: 100%;
  gap: 12px; /* 减小间隙 */
  animation: scrollGallery 35s linear infinite;
}
.scrolling-photos:hover { animation-play-state: paused; }
.photo-item {
  flex: 0 0 auto;
  width: 190px; /* 减小宽度以匹配新高度 */
  height: 100%;
  border-radius: 4px;
  overflow: hidden;
  box-shadow: 0 2px 5px rgba(0,0,0,0.07);
  transition: transform 0.35s cubic-bezier(0.175, 0.885, 0.32, 1.275), box-shadow 0.35s ease;
  position: relative;
  z-index: 1;
  padding: 3px;
  background: white;
  border: 1px solid #e0e0e0;
}
.photo-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0.02) 100%);
  pointer-events: none;
}
.photo-item:hover { 
  transform: translateY(-8px) scale(1.02); /* 减小悬停效果 */
  box-shadow: 0 12px 20px rgba(0,0,0,0.12), 0 0 0 1.5px rgba(52, 152, 219, 0.2);
  border-color: #3498db;
  z-index: 10;
}
.photo-inner {
  width: 100%;
  height: 100%;
  border-radius: 2px;
  overflow: hidden;
  position: relative;
  box-shadow: inset 0 0 2px rgba(0,0,0,0.06);
  transform: translateZ(0);
  -webkit-transform: translateZ(0);
}
.photo-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s cubic-bezier(0.215, 0.610, 0.355, 1);
  image-rendering: -webkit-optimize-contrast;
  image-rendering: crisp-edges;
  -ms-interpolation-mode: nearest-neighbor;
  transform: translateZ(0);
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.photo-item:hover .photo-img { 
  transform: scale(1.12) translateZ(0); /* 减小放大效果 */
}
.photo-label {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.85), rgba(0,0,0,0.55));
  color: white;
  padding: 5px;
  font-size: 0.75rem;
  text-align: center;
  transform: translateY(100%);
  transition: transform 0.25s ease;
  backdrop-filter: blur(1px);
}
.photo-item:hover .photo-label { 
  transform: translateY(0); 
}
@keyframes scrollGallery {
  0% { transform: translateX(0); }
  100% { transform: translateX(calc(-190px * 10 - 12px * 10)); } /* 更新为190px */
}

/* 响应式设计 - 调整移动端 */
@media (max-width: 768px) {
  .photo-frame { 
    height: 180px; /* 移动端减小 */
    padding: 3px;
  }
  .photo-item { 
    width: 130px; /* 移动端宽度相应调整 */
    padding: 2px;
  }
  .gallery-title { 
    font-size: 0.95rem; 
    margin-bottom: 6px;
    padding: 6px;
  }
  .photo-item:hover { 
    transform: translateY(-4px) scale(1.01); 
    box-shadow: 0 8px 14px rgba(0,0,0,0.1), 0 0 0 1px rgba(52, 152, 219, 0.15);
  }
  .photo-item:hover .photo-img { 
    transform: scale(1.08) translateZ(0); 
  }
  @keyframes scrollGallery {
    0% { transform: translateX(0); }
    100% { transform: translateX(calc(-130px * 10 - 12px * 10)); } /* 更新为130px */
  }
}
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div class="photo-gallery-container">
  <h2 class="gallery-title">
    <i class="fas fa-images"></i>
    Be true to yourself, and respect others.
  </h2>
  
  <div class="photo-frame">
    <div class="scrolling-photos" id="scrollingPhotos"></div>
  </div>
</div>

<script>
const photos = [
  { 
    url: "https://Zuojie-Li.github.io/files/M1.jpg", 
    title: "泰安", 
    desc: "东平湖" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M3.jpg", 
    title: "", 
    desc: "" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M4.jpg", 
    title: "", 
    desc: "" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M5.jpg", 
    title: "", 
    desc: "" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M6.jpg", 
    title: "", 
    desc: "" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M7.jpg", 
    title: "", 
    desc: "" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M2.jpg", 
    title: "泰安", 
    desc: "东平湖" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M8.jpg", 
    title: "", 
    desc: "" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M9.jpg", 
    title: "", 
    desc: "" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M10.jpg", 
    title: "", 
    desc: "" 
  }
];

const scrollingPhotos = document.getElementById('scrollingPhotos');

[...photos, ...photos].forEach((photo, index) => {
  const photoItem = document.createElement('div');
  photoItem.className = 'photo-item';
  photoItem.innerHTML = `
    <div class="photo-inner">
      <img src="${photo.url}" alt="${photo.title}" class="photo-img" loading="lazy">
      <div class="photo-label"><strong>${photo.title}</strong><br><small>${photo.desc}</small></div>
    </div>
  `;
  scrollingPhotos.appendChild(photoItem);
});
</script>
