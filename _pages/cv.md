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
<!-- 滚动相框组件 - 添加到Markdown文档底部 -->
<style>
  .photo-gallery-container {
    background-color: white;
    border-radius: 12px;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
    padding: 20px;
    margin: 15px 0 20px 0;
    border-top: 4px solid #3498db;
  }
  
  .gallery-title {
    font-size: 1.6rem;
    color: #2c3e50;
    margin: 0 0 15px 0;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
  }
  
  .photo-frame {
    width: 100%;
    height: 250px;
    background: linear-gradient(145deg, #f0f0f0, #ffffff);
    border-radius: 10px;
    padding: 12px;
    box-shadow: inset 0 0 8px rgba(0, 0, 0, 0.05);
    position: relative;
    overflow: hidden;
  }
  
  .photo-frame::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 6px;
    background: linear-gradient(90deg, #3498db, #2ecc71, #e74c3c, #f39c12, #9b59b6);
    z-index: 2;
  }
  
  .scrolling-photos {
    display: flex;
    height: 100%;
    gap: 18px;
    animation: scrollGallery 40s linear infinite;
  }
  
  .scrolling-photos:hover {
    animation-play-state: paused;
  }
  
  .photo-item {
    flex: 0 0 auto;
    width: 200px;
    height: 100%;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    position: relative;
  }
  
  .photo-item:hover {
    transform: translateY(-6px);
    box-shadow: 0 10px 18px rgba(0, 0, 0, 0.12);
  }
  
  .photo-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
  }
  
  .photo-item:hover .photo-img {
    transform: scale(1.05);
  }
  
  .photo-label {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 8px;
    font-size: 0.85rem;
    text-align: center;
    transform: translateY(100%);
    transition: transform 0.3s ease;
  }
  
  .photo-item:hover .photo-label {
    transform: translateY(0);
  }
  
  .controls {
    display: flex;
    justify-content: center;
    gap: 12px;
    margin-top: 15px;
  }
  
  .control-btn {
    background-color: #3498db;
    color: white;
    border: none;
    padding: 8px 16px;
    border-radius: 50px;
    cursor: pointer;
    font-size: 0.9rem;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 6px;
    box-shadow: 0 3px 5px rgba(52, 152, 219, 0.2);
  }
  
  .control-btn:hover {
    background-color: #2980b9;
    transform: translateY(-2px);
    box-shadow: 0 5px 7px rgba(52, 152, 219, 0.3);
  }
  
  .photo-counter {
    text-align: center;
    margin-top: 12px;
    color: #7f8c8d;
    font-size: 0.9rem;
  }
  
  @keyframes scrollGallery {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(calc(-200px * 10 - 18px * 10));
    }
  }
  
  @media (max-width: 768px) {
    .photo-gallery-container {
      padding: 15px;
      margin: 10px 0 15px 0;
    }
    
    .gallery-title {
      font-size: 1.4rem;
      margin: 0 0 12px 0;
    }
    
    .photo-frame {
      height: 200px;
      padding: 10px;
    }
    
    .photo-item {
      width: 160px;
    }
    
    .controls {
      margin-top: 12px;
      gap: 10px;
    }
    
    .control-btn {
      padding: 7px 14px;
      font-size: 0.85rem;
    }
    
    @keyframes scrollGallery {
      0% {
        transform: translateX(0);
      }
      100% {
        transform: translateX(calc(-160px * 10 - 18px * 10));
      }
    }
  }
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div class="photo-gallery-container">
  <h2 class="gallery-title">
    <i class="fas fa-camera-retro"></i> 精彩瞬间相册
  </h2>
  
  <div class="photo-frame">
    <div class="scrolling-photos" id="scrollingPhotos">
      <!-- 图片将通过JavaScript动态添加 -->
    </div>
  </div>
  
  <div class="controls">
    <button class="control-btn" id="pauseBtn">
      <i class="fas fa-pause"></i> 暂停滚动
    </button>
    <button class="control-btn" id="playBtn">
      <i class="fas fa-play"></i> 继续滚动
    </button>
    <button class="control-btn" id="reverseBtn">
      <i class="fas fa-backward"></i> 反向滚动
    </button>
  </div>
  
  <div class="photo-counter">
    展示中: <span id="currentPhoto">1</span> / <span id="totalPhotos">10</span> 张图片
  </div>
</div>

<script>
  // 图片数据 - 可以替换为您自己的图片
  const photos = [
    { 
      url: "https://images.unsplash.com/photo-1501854140801-50d01698950b?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "山间日出", 
      desc: "美丽的清晨山景" 
    },
    { 
      url: "https://images.unsplash.com/photo-1439066615861-d1af74d74000?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "湖畔森林", 
      desc: "宁静的湖边森林" 
    },
    { 
      url: "https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "迷雾山脉", 
      desc: "云雾缭绕的山峦" 
    },
    { 
      url: "https://images.unsplash.com/photo-1465146344425-f00d5f5c8f07?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "自然小径", 
      desc: "穿越森林的小路" 
    },
    { 
      url: "https://images.unsplash.com/photo-1426604966848-d7adac402bff?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "瀑布风光", 
      desc: "壮观的瀑布景色" 
    },
    { 
      url: "https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "雪山峰顶", 
      desc: "雄伟的雪山景观" 
    },
    { 
      url: "https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "秋日森林", 
      desc: "金黄色的秋天树林" 
    },
    { 
      url: "https://images.unsplash.com/photo-1475924156734-496f6cac6ec1?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "海岸日落", 
      desc: "海滩上的日落美景" 
    },
    { 
      url: "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "冰川湖泊", 
      desc: "清澈的冰川湖" 
    },
    { 
      url: "https://images.unsplash.com/photo-1519681393784-d120267933ba?w=500&h=350&fit=crop&crop=entropy&auto=format", 
      title: "星空夜景", 
      desc: "璀璨的夜空星辰" 
    }
  ];

  // 初始化相册
  const scrollingPhotos = document.getElementById('scrollingPhotos');
  const totalPhotosElement = document.getElementById('totalPhotos');
  const currentPhotoElement = document.getElementById('currentPhoto');
  
  // 设置总图片数
  totalPhotosElement.textContent = photos.length;
  
  // 为了创建无缝滚动效果，我们将图片复制一份
  const allPhotos = [...photos, ...photos];
  
  // 动态生成图片元素
  allPhotos.forEach((photo, index) => {
    const photoItem = document.createElement('div');
    photoItem.className = 'photo-item';
    photoItem.dataset.index = (index % photos.length) + 1;
    
    photoItem.innerHTML = `
      <img src="${photo.url}" 
           alt="${photo.title}" 
           class="photo-img">
      <div class="photo-label">
        <strong>${photo.title}</strong><br>
        <small>${photo.desc}</small>
      </div>
    `;
    
    scrollingPhotos.appendChild(photoItem);
  });
  
  // 控制按钮功能
  const pauseBtn = document.getElementById('pauseBtn');
  const playBtn = document.getElementById('playBtn');
  const reverseBtn = document.getElementById('reverseBtn');
  
  let isPaused = false;
  let isReversed = false;
  
  pauseBtn.addEventListener('click', () => {
    scrollingPhotos.style.animationPlayState = 'paused';
    isPaused = true;
  });
  
  playBtn.addEventListener('click', () => {
    scrollingPhotos.style.animationPlayState = 'running';
    isPaused = false;
  });
  
  reverseBtn.addEventListener('click', () => {
    isReversed = !isReversed;
    if (isReversed) {
      scrollingPhotos.style.animationDirection = 'reverse';
      reverseBtn.innerHTML = '<i class="fas fa-forward"></i> 正向滚动';
    } else {
      scrollingPhotos.style.animationDirection = 'normal';
      reverseBtn.innerHTML = '<i class="fas fa-backward"></i> 反向滚动';
    }
  });
  
  // 更新当前显示的图片
  let currentVisibleIndex = 1;
  
  const updateCurrentPhoto = () => {
    if (isPaused) return;
    
    if (isReversed) {
      currentVisibleIndex--;
      if (currentVisibleIndex < 1) currentVisibleIndex = photos.length;
    } else {
      currentVisibleIndex++;
      if (currentVisibleIndex > photos.length) currentVisibleIndex = 1;
    }
    
    currentPhotoElement.textContent = currentVisibleIndex;
  };
  
  // 每4秒更新一次当前图片指示器
  setInterval(updateCurrentPhoto, 4000);
  
  // 初始设置
  scrollingPhotos.style.animation = `scrollGallery 40s linear infinite`;
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
