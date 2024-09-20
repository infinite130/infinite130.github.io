---
layout: none
title: "Portfolio"
permalink: /portfolio/
main_nav: true
---

<link rel="stylesheet" href="{{ site.baseurl }}/css/style.css"> <!-- CSS 파일 링크 -->
<link href='https://fonts.googleapis.com/css?family=Lato:400,300,700' rel='stylesheet' type='text/css'>

<div class="container">
  <div class="header">
    <div class="full-name">
      <span class="first-name">이나래</span>
      <br>
    </div>
    <div class="contact-info">
      <span class="email">Email </span>
      <span class="email-val">skfo3219@gmail.com</span><br>
  
      <span class="github">GitHub </span>
      <span class="github-val">
        <a href="https://github.com/infinite130" target="_blank" rel="noopener noreferrer">infinite130</a>
      </span><br>

      <span class="blog">Blog </span>
      <span class="blog-val">
        <a href="https://infinite130.github.io" target="_blank" rel="noopener noreferrer">infinite130.github.io</a>
      </span>
    </div>

    <div class="about">
      <span class="position">Java Junior Back-End Developer </span>
      <br>
      <span class="desc">
        안녕하세요. 백엔드 개발자가 되고 싶은 이나래입니다.
        저는 원래 바리스타로 근무하면서 음료를 제조하고 고객과 소통하는 일을 3년간 
      </span>
    </div>
  </div>

  <div class="details">
    <div class="section">
      <div class="section__title">Projects</div> 
      <div class="section__list">
        <!-- 첫 번째 프로젝트 -->
        <div class="section__list-item">
          <div class="name">팀 프로젝트 마이그레이션</div>
          <!-- 이미지 슬라이드 -->
          <div class="carousel" id="carousel1">
            <button class="prev" onclick="changeSlide(-1, 'carousel1')">&#10094;</button>
            <div class="slides">
              <img src="https://github.com/user-attachments/assets/82450a17-54ad-424e-a0ab-c494fbe8bd3f" alt="Slide 1" class="active">
              <img src="https://github.com/user-attachments/assets/682026b2-a978-4f13-83a2-76d69b79ca58" alt="Slide 2">
            </div>
            <button class="next" onclick="changeSlide(1, 'carousel1')">&#10095;</button>
          </div>

          <!-- 프로젝트 기간 및 사용기술 -->
          <div class="project-info">
            <p><strong>기간:</strong> 2024년 9월 - 진행중</p>
            <p><strong>사용 기술:</strong></p>
            <div class="tech-stack">
              <img src="https://img.shields.io/badge/spring-6DB33F?logo=spring&logoColor=white">
              <img src="https://img.shields.io/badge/eclipse-2C2255?style=flat-square&logo=eclipse&logoColor=white">
              <img src="https://img.shields.io/badge/maven-C71A36?logo=apache-maven&logoColor=white">
              <img src="https://img.shields.io/badge/mybatis-DC382D?logo=mybatis&logoColor=white"/>
              <img src="https://img.shields.io/badge/html5-E34F26?logo=html5&logoColor=white">
              <img src="https://img.shields.io/badge/javascript-F7DF1E?logo=javascript&logoColor=black">
            </div>
          </div>

          <div class="text">I am a front-end developer with more than 3 years of experience writing html, css, and js. I'm motivated, result-focused and seeking a successful team-oriented company with opportunity to grow.</div>
          <a href="https://github.com/your-repo-url" target="_blank">GitHub 이동</a>
          <a href="https://yoursite.com" target="_blank">사이트 이동</a>
        </div>

        <!-- 두 번째 프로젝트 -->
        <div class="section__list-item">
          <div class="name">SML</div>
          <div class="carousel" id="carousel2">
            <button class="prev" onclick="changeSlide(-1, 'carousel2')">&#10094;</button>
            <div class="slides">
              <img src="https://github.com/user-attachments/assets/82450a17-54ad-424e-a0ab-c494fbe8bd3f" alt="Slide 1" class="active">
              <img src="https://github.com/user-attachments/assets/682026b2-a978-4f13-83a2-76d69b79ca58" alt="Slide 2">
            </div>
            <button class="next" onclick="changeSlide(1, 'carousel2')">&#10095;</button>
          </div>

          <!-- 프로젝트 기간 및 사용기술 -->
          <div class="project-info">
            <p><strong>기간:</strong> 2022년 9월 - 2023년 1월</p>
            <p><strong>사용 기술:</strong> Python, Django, PostgreSQL</p>
          </div>

          <div class="text">I am a front-end developer with more than 3 years of experience writing html, css, and js. I'm motivated, result-focused and seeking a successful team-oriented company with opportunity to grow. </div>
          <a href="https://github.com/SML-SpringInMyLife/SML" target="_blank">GitHub 이동</a>
        </div>

        <!-- 세 번째 프로젝트 -->
        <div class="section__list-item">
          <div class="name">JAVANOS</div>
          <div class="carousel" id="carousel3">
            <button class="prev" onclick="changeSlide(-1, 'carousel3')">&#10094;</button>
            <div class="slides">
              <img src="https://github.com/user-attachments/assets/82450a17-54ad-424e-a0ab-c494fbe8bd3f" alt="Slide 1" class="active">
              <img src="https://github.com/user-attachments/assets/682026b2-a978-4f13-83a2-76d69b79ca58" alt="Slide 2">
            </div>
            <button class="next" onclick="changeSlide(1, 'carousel3')">&#10095;</button>
          </div>

          <!-- 프로젝트 기간 및 사용기술 -->
          <div class="project-info">
            <p><strong>기간:</strong> 2021년 10월 - 2022년 3월</p>
            <p><strong>사용 기술:</strong> Java, Spring Framework, Oracle DB</p>
          </div>

          <div class="text">I am a front-end developer with more than 3 years of experience writing html, css, and js. I'm motivated, result-focused and seeking a successful team-oriented company with opportunity to grow.</div>
          <a href="https://github.com/JAVANOS6/javanos" target="_blank">GitHub 이동</a>
        </div>
      </div>
    </div>
    
    <!-- Skills 섹션 -->
    <div class="section">
      <div class="section__title">Skills</div>
      <div class="section__list">
        <div class="section__list-item">
          <div class="name">Javascript</div>
        </div>
        <div class="section__list-item">
          <div class="name">CSS</div>
        </div>
        <div class="section__list-item">
          <div class="name">HTML</div>
        </div>
      </div>
    </div>

    <!-- Experience 섹션 -->
    <div class="section">
      <div class="section__title">Experience</div>
      <div class="section__list">
        <div class="section__list-item">
          <div class="name">KlowdBox</div>
          <div class="project-info">
            <p><strong>기간:</strong> Jan 2011 - Feb 2015</p>
            <p><strong>역할:</strong> Fr developer</p>
          </div>
          <div class="text">did This and that</div>
        </div>
        <div class="section__list-item">
          <div class="name">Akount</div>
          <div class="project-info">
            <p><strong>기간:</strong> Jan 2011 - Feb 2015</p>
            <p><strong>역할:</strong> Fr developer</p>
          </div>
          <div class="text">did This and that</div>
        </div>
      </div>
    </div>

    <!-- Education 섹션 -->
    <div class="section">
      <div class="section__title">Education</div>
      <div class="section__list">
        <div class="section__list-item">
          <div class="name">Sample Institute of Technology</div>
          <div class="project-info">
            <p><strong>기간:</strong> Jan 2011 - Feb 2015</p>
            <p><strong>학위:</strong> Fr developer</p>
          </div>
          <div class="text">did This and that</div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- 슬라이드 스타일 -->
<style>
.container {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
}

.section__title {
  font-size: 24px;
  margin-bottom: 20px;
}

.section__list-item {
  margin-bottom: 40px; /* 프로젝트 간격 */
}

.carousel {
  position: relative;
  max-width: 600px; /* 슬라이드 전체 크기를 줄임 */
  margin-bottom: 20px; /* 슬라이드 아래 간격 */
}

.slides img {
  display: none;
  width: 100%; /* 슬라이드 안에서 이미지가 전체 크기로 */
}

.slides img.active {
  display: block;
}

.prev, .next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
}

.prev {
  left: 0;
}

.next {
  right: 0;
}

.project-info {
  margin: 15px 0;
  font-size: 14px;
}

.tech-stack img {
  margin-right: 10px;
  vertical-align: middle;
}
</style>

<!-- 슬라이드 기능 자바스크립트 -->
<script>
function changeSlide(n, carouselId) {
  let slides = document.querySelectorAll(`#${carouselId} .slides img`);
  let activeIndex = Array.from(slides).findIndex(slide => slide.classList.contains('active'));
  
  slides[activeIndex].classList.remove('active');
  
  let newIndex = activeIndex + n;
  if (newIndex >= slides.length) newIndex = 0;
  if (newIndex < 0) newIndex = slides.length - 1;
  
  slides[newIndex].classList.add('active');
}
</script>
