---
layout: default
title: 진료 안내
permalink: /treatments
---

<!-- TODO: 배경 이미지 추가 - hero-services.jpg (정갈하게 정리된 진료 도구나 원장님의 진료 상담 모습) -->
<section class="hero-wide">
  <div class="hero-wide-overlay"></div>
  <div class="hero-wide-content">
    <p class="hero-wide-subtitle">MEDICAL SERVICE</p>
    <h1 class="hero-wide-title">일상을 되찾는 치료, 내 몸에 맞게</h1>
    <p class="hero-wide-sub">통증·피로·컨디션까지 개인별로 섬세하게</p>
  </div>
</section>

<div class="treatment-container">
    <div class="treatment-grid">
        <div class="treatment-card">
            <div class="card-header">
                <span class="category-icon">🦴</span>
                <h2>통증 재활</h2>
            </div>
            <ul class="treatment-list">
                <li>척추 · 관절</li>
                <li>교통사고 후유증</li>
            </ul>
        </div>

        <div class="treatment-card">
            <div class="card-header">
                <span class="category-icon">🌿</span>
                <h2>기능 회복</h2>
            </div>
            <ul class="treatment-list">
                <li>안면마비</li>
                <li>난청 · 난임</li>
            </ul>
        </div>

        <div class="treatment-card">
            <div class="card-header">
                <span class="category-icon">✨</span>
                <h2>미용 한방</h2>
            </div>
            <ul class="treatment-list">
                <li>매선 / 피부</li>
                <li>체형 관리</li>
            </ul>
        </div>
    </div>

    <div class="treatment-footer">
        <p>※ 제일한의원은 환자 한 분 한 분의 증상에 맞춘 <strong>설명 가능한 진단</strong>과 <strong>납득되는 치료</strong>를 약속합니다.</p>
    </div>
</div>

<style>
/* 진료 안내 전용 스타일 */
.treatment-container {
    max-width: 1100px;
    margin: 60px auto;
    padding: 0 20px;
}

.treatment-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.treatment-card {
    background: #ffffff;
    border-radius: 15px;
    padding: 40px 30px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.05);
    border: 1px solid #f0f0f0;
    transition: transform 0.3s ease;
}

.treatment-card:hover {
    transform: translateY(-5px);
}

.card-header {
    margin-bottom: 25px;
    padding-bottom: 15px;
    border-bottom: 2px solid #1a237e; /* 의료진 소개 페이지와 통일감 있는 네이비 */
}

.category-icon {
    font-size: 2rem;
    display: block;
    margin-bottom: 10px;
}

.treatment-card h2 {
    font-size: 1.5rem;
    font-weight: 700;
    color: #1a237e;
    margin: 0;
}

.treatment-list {
    list-style: none;
    padding: 0;
    margin: 0;
}

.treatment-list li {
    padding: 10px 0;
    font-size: 1.15rem;
    color: #444;
    position: relative;
    padding-left: 25px;
}

.treatment-list li::before {
    content: "•";
    color: #1a237e;
    font-weight: bold;
    position: absolute;
    left: 0;
}

.treatment-footer {
    margin-top: 60px;
    text-align: center;
    padding: 30px;
    background: #f8f9fa;
    border-radius: 10px;
    color: #666;
    line-height: 1.6;
}

@media (max-width: 768px) {
    .treatment-grid {
        grid-template-columns: 1fr;
    }
}
</style>