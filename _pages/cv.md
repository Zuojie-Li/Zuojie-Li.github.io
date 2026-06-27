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
* Born: December 1996
* Native place: Tai'an, Shandong Province​
* Party: Member of the Communist Party of China
* Workplace: Key Laboratory of Radiopharmaceuticals / Beam Technology of the Ministry of Education, Beijing Normal University

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
* J Med Chem, 2026, 69(5),  5887–5900.
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
<!-- 滚动相框组件 - 高清优化版 -->
<style>
.photo-gallery-container {
  background: white;
  border-radius: 8px;
  box-shadow: 0 3px 12px rgba(0,0,0,0.08);
  padding: 12px;
  margin: 10px 0;
  border-top: 3px solid #3498db;
}
.gallery-title {
  font-size: 1.2rem;
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
  text-shadow: 0 0 15px rgba(255, 255, 255, 0.3);
  margin: 0 0 12px 0;
  padding: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}
@keyframes softRainbow {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

/* 主要修改：相框高度从240px增加到320px */
.photo-frame {
  height: 320px; /* 已调大：从240px增加到320px */
  background: #f8f9fa;
  border-radius: 6px;
  padding: 6px;
  position: relative;
  overflow: hidden;
}
.photo-frame::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, #3498db, #2ecc71, #e74c3c);
}
.scrolling-photos {
  display: flex;
  height: 100%;
  gap: 15px;
  animation: scrollGallery 35s linear infinite;
}
.scrolling-photos:hover { animation-play-state: paused; }
.photo-item {
  flex: 0 0 auto;
  width: 230px; /* 略微增加宽度以匹配更高高度 */
  height: 100%;
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
  transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275), box-shadow 0.4s ease;
  position: relative;
  z-index: 1;
  padding: 4px;
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
  transform: translateY(-10px) scale(1.03); 
  box-shadow: 0 15px 25px rgba(0,0,0,0.15), 0 0 0 2px rgba(52, 152, 219, 0.2);
  border-color: #3498db;
  z-index: 10;
}
.photo-inner {
  width: 100%;
  height: 100%;
  border-radius: 3px;
  overflow: hidden;
  position: relative;
  box-shadow: inset 0 0 3px rgba(0,0,0,0.08);
  /* 添加GPU加速 */
  transform: translateZ(0);
  -webkit-transform: translateZ(0);
}
.photo-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s cubic-bezier(0.215, 0.610, 0.355, 1);
  /* 优化图片渲染质量 */
  image-rendering: -webkit-optimize-contrast;
  image-rendering: crisp-edges;
  -ms-interpolation-mode: nearest-neighbor;
  /* 避免图片模糊的关键设置 */
  transform: translateZ(0);
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.photo-item:hover .photo-img { 
  transform: scale(1.15) translateZ(0); 
}
.photo-label {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.85), rgba(0,0,0,0.55));
  color: white;
  padding: 6px;
  font-size: 0.8rem;
  text-align: center;
  transform: translateY(100%);
  transition: transform 0.3s ease;
  backdrop-filter: blur(1px);
}
.photo-item:hover .photo-label { 
  transform: translateY(0); 
}
@keyframes scrollGallery {
  0% { transform: translateX(0); }
  100% { transform: translateX(calc(-230px * 10 - 15px * 10)); } /* 更新为230px */
}

/* 响应式设计 - 调整移动端高度 */
@media (max-width: 768px) {
  .photo-frame { 
    height: 220px; /* 移动端也相应调高 */
    padding: 4px;
  }
  .photo-item { 
    width: 160px; /* 移动端宽度相应调整 */
    padding: 3px;
  }
  .gallery-title { 
    font-size: 1rem; 
    margin-bottom: 8px;
    padding: 8px;
  }
  .photo-item:hover { 
    transform: translateY(-6px) scale(1.02); 
    box-shadow: 0 10px 18px rgba(0,0,0,0.12), 0 0 0 1px rgba(52, 152, 219, 0.2);
  }
  .photo-item:hover .photo-img { 
    transform: scale(1.12) translateZ(0); 
  }
  @keyframes scrollGallery {
    0% { transform: translateX(0); }
    100% { transform: translateX(calc(-160px * 10 - 15px * 10)); } /* 更新为160px */
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
    title: "北京", 
    desc: "樱花园" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M4.jpg", 
    title: "北京", 
    desc: "海晏堂" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M5.jpg", 
    title: "北京", 
    desc: "玉渊潭" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M6.jpg", 
    title: "北京", 
    desc: "黄花阵" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M7.jpg", 
    title: "西安", 
    desc: "钟楼" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M2.jpg", 
    title: "泰安", 
    desc: "东平湖" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M8.jpg", 
    title: "北京", 
    desc: "中关村" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M9.jpg", 
    title: "北京", 
    desc: "西洋楼" 
  },
  { 
    url: "https://Zuojie-Li.github.io/files/M10.jpg", 
    title: "北京", 
    desc: "圆明园" 
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
