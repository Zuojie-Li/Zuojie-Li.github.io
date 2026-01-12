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
<!-- 滚动相框组件 - 优化图片尺寸版 -->
<style>
.photo-gallery-container {
  background: white;
  border-radius: 8px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.08);
  padding: 12px;
  margin: 8px 0;
  border-top: 2px solid #3498db;
}
.gallery-title {
  font-size: 1.2rem;
  color: #2c3e50;
  margin: 0 0 10px 0;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
}
.photo-frame {
  height: 200px;
  background: #f8f9fa;
  border-radius: 6px;
  padding: 8px;
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
  animation: scrollGallery 30s linear infinite;
}
.scrolling-photos:hover { animation-play-state: paused; }
.photo-item {
  flex: 0 0 auto;
  width: 170px;
  height: 100%;
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
  transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275), box-shadow 0.4s ease;
  position: relative;
  z-index: 1;
  padding: 8px;
  background: white;
  border: 1px solid #eaeaea;
}
.photo-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, rgba(255,255,255,0.2) 0%, rgba(255,255,255,0.05) 100%);
  pointer-events: none;
}
.photo-item:hover { 
  transform: translateY(-12px) scale(1.03); 
  box-shadow: 0 15px 25px rgba(0,0,0,0.15), 0 0 0 3px rgba(52, 152, 219, 0.2);
  border-color: #3498db;
  z-index: 10;
}
.photo-inner {
  width: 100%;
  height: 100%;
  border-radius: 3px;
  overflow: hidden;
  position: relative;
  box-shadow: inset 0 0 5px rgba(0,0,0,0.1);
}
.photo-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s cubic-bezier(0.215, 0.610, 0.355, 1);
}
.photo-item:hover .photo-img { 
  transform: scale(1.15); 
}
.photo-label {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.9), rgba(0,0,0,0.6));
  color: white;
  padding: 8px;
  font-size: 0.8rem;
  text-align: center;
  transform: translateY(100%);
  transition: transform 0.4s ease;
  backdrop-filter: blur(2px);
}
.photo-item:hover .photo-label { 
  transform: translateY(0); 
}
@keyframes scrollGallery {
  0% { transform: translateX(0); }
  100% { transform: translateX(calc(-170px * 10 - 15px * 10)); }
}
@media (max-width: 768px) {
  .photo-frame { height: 160px; }
  .photo-item { width: 140px; }
  .gallery-title { font-size: 1.1rem; margin-bottom: 8px; }
  .photo-item:hover { 
    transform: translateY(-8px) scale(1.02); 
    box-shadow: 0 10px 18px rgba(0,0,0,0.12), 0 0 0 2px rgba(52, 152, 219, 0.2);
  }
  .photo-item:hover .photo-img { 
    transform: scale(1.12); 
  }
  @keyframes scrollGallery {
    0% { transform: translateX(0); }
    100% { transform: translateX(calc(-140px * 10 - 15px * 10)); }
  }
}
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div class="photo-gallery-container">
  <h2 class="gallery-title"><i class="fas fa-images"></i>相册</h2>
  <div class="photo-frame">
    <div class="scrolling-photos" id="scrollingPhotos"></div>
  </div>
</div>

<script>
const photos = [
  { 
    url: "https://Zuojie-Li.github.io/files/M1.jpg", 
    title: "山间日出", 
    desc: "清晨山景" 
  },
  { 
    url: "https://images.unsplash.com/photo-1439066615861-d1af74d74000?w=400&h=300&fit=crop&auto=format", 
    title: "湖畔森林", 
    desc: "湖边森林" 
  },
  { 
    url: "https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?w=400&h=300&fit=crop&auto=format", 
    title: "迷雾山脉", 
    desc: "云雾山峦" 
  },
  { 
    url: "https://images.unsplash.com/photo-1465146344425-f00d5f5c8f07?w=400&h=300&fit=crop&auto=format", 
    title: "自然小径", 
    desc: "森林小路" 
  },
  { 
    url: "https://images.unsplash.com/photo-1426604966848-d7adac402bff?w=400&h=300&fit=crop&auto=format", 
    title: "瀑布风光", 
    desc: "瀑布景色" 
  },
  { 
    url: "https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=400&h=300&fit=crop&auto=format", 
    title: "雪山峰顶", 
    desc: "雪山景观" 
  },
  { 
    url: "https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=400&h=300&fit=crop&auto=format", 
    title: "秋日森林", 
    desc: "秋天树林" 
  },
  { 
    url: "https://images.unsplash.com/photo-1475924156734-496f6cac6ec1?w=400&h=300&fit=crop&auto=format", 
    title: "海岸日落", 
    desc: "日落美景" 
  },
  { 
    url: "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=400&h=300&fit=crop&auto=format", 
    title: "冰川湖泊", 
    desc: "冰川湖" 
  },
  { 
    url: "https://images.unsplash.com/photo-1519681393784-d120267933ba?w=400&h=300&fit=crop&auto=format", 
    title: "星空夜景", 
    desc: "夜空星辰" 
  }
];

const scrollingPhotos = document.getElementById('scrollingPhotos');

[...photos, ...photos].forEach((photo, index) => {
  const photoItem = document.createElement('div');
  photoItem.className = 'photo-item';
  photoItem.innerHTML = `
    <div class="photo-inner">
      <img src="${photo.url}" alt="${photo.title}" class="photo-img">
      <div class="photo-label"><strong>${photo.title}</strong><br><small>${photo.desc}</small></div>
    </div>
  `;
  scrollingPhotos.appendChild(photoItem);
});
</script>

<div style="
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
    text-align: left;
    padding: 20px;
    font-family: 'Helvetica Neue', sans-serif;
    text-shadow: 0 0 15px rgba(255, 255, 255, 0.3);
">
    Be true to yourself, and respect others.
</div>

<style>
@keyframes softRainbow {
    0%, 100% {
        background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
}
</style>

<div id="cute-animation" style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    width: 150px;
    height: 150px;
    z-index: 1000;
    pointer-events: none;
">
    <!-- 小猫动画 -->
    <div style="
        position: absolute;
        width: 60px;
        height: 60px;
        animation: floatCat 6s ease-in-out infinite;
    ">
        <div style="
            position: absolute;
            width: 40px;
            height: 30px;
            background: #FFB6C1;
            border-radius: 50% 50% 40% 40%;
            top: 0;
            left: 10px;
        "></div>
        <div style="
            position: absolute;
            width: 10px;
            height: 10px;
            background: black;
            border-radius: 50%;
            top: 10px;
            left: 20px;
        "></div>
        <div style="
            position: absolute;
            width: 10px;
            height: 10px;
            background: black;
            border-radius: 50%;
            top: 10px;
            left: 30px;
        "></div>
    </div>
    
    <!-- 小狗动画 -->
    <div style="
        position: absolute;
        width: 60px;
        height: 60px;
        animation: floatDog 8s ease-in-out infinite 1s;
    ">
        <div style="
            position: absolute;
            width: 40px;
            height: 30px;
            background: #FFD700;
            border-radius: 50% 50% 40% 40%;
            top: 0;
            left: 10px;
        "></div>
        <div style="
            position: absolute;
            width: 25px;
            height: 15px;
            background: #FFD700;
            border-radius: 50%;
            top: 5px;
            left: 0;
            transform: rotate(-20deg);
        "></div>
    </div>
</div>

<style>
@keyframes floatCat {
    0%, 100% {
        transform: translate(0, 0) rotate(0deg);
    }
    25% {
        transform: translate(30px, -40px) rotate(5deg);
    }
    50% {
        transform: translate(60px, 0) rotate(0deg);
    }
    75% {
        transform: translate(30px, -40px) rotate(-5deg);
    }
}

@keyframes floatDog {
    0%, 100% {
        transform: translate(80px, 0) rotate(0deg);
    }
    25% {
        transform: translate(50px, -50px) rotate(5deg);
    }
    50% {
        transform: translate(20px, 0) rotate(0deg);
    }
    75% {
        transform: translate(50px, -50px) rotate(-5deg);
    }
}

@keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
        transform: translateY(0);
    }
    40% {
        transform: translateY(-20px);
    }
    60% {
        transform: translateY(-10px);
    }
}

@keyframes pulse {
    0%, 100% {
        transform: scale(1);
        opacity: 1;
    }
    50% {
        transform: scale(1.1);
        opacity: 0.8;
    }
}

@keyframes heartbeat {
    0%, 100% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.1);
    }
}

@keyframes twinkle {
    0%, 100% {
        opacity: 1;
        transform: scale(1);
    }
    50% {
        opacity: 0.5;
        transform: scale(0.9);
    }
}
</style>
