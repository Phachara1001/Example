<script setup>
const features = [
  {
    title: 'ออกแบบสวยงาม',
    description: 'หน้าเว็บเรียบง่าย ใช้งานได้ทั้งบนเดสก์ท็อปและมือถือ',
  },
  {
    title: 'เร็วและทันใจ',
    description: 'โหลดเร็วด้วย Vite พร้อมโค้ด Vue 3 ที่ทันสมัย',
  },
  {
    title: 'ปรับแต่งได้ทันที',
    description: 'เปลี่ยนข้อความ สี หรือส่วนประกอบได้ง่าย ๆ',
  },
]
</script>

<template>
  <div id="app">
    <header class="site-header">
      <div class="brand">ตัวอย่างเว็บไซต์</div>
      <nav>
        <a href="#features">ฟีเจอร์</a>
        <a href="#about">เกี่ยวกับ</a>
        <a href="#contact">ติดต่อ</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="hero-copy">
          <p class="eyebrow">เว็บไซต์ตัวอย่าง</p>
          <h1>สร้างเว็บไซต์สวยทันสมัยด้วย Vue และ Vite</h1>
          <p class="hero-text">
            แสดงตัวอย่างเว็บที่พร้อมใช้งาน พร้อมแผงฟีเจอร์และปุ่มติดต่อสื่อสาร
          </p>
          <div class="hero-actions">
            <a class="button primary" href="#contact">ติดต่อเรา</a>
            <a class="button secondary" href="#features">ดูฟีเจอร์</a>
          </div>
        </div>
      </section>

      <section id="features" class="section features">
        <h2>สิ่งที่คุณจะได้</h2>
        <div class="feature-grid">
          <article v-for="feature in features" :key="feature.title" class="feature-card">
            <h3>{{ feature.title }}</h3>
            <p>{{ feature.description }}</p>
          </article>
        </div>
      </section>

      <section id="about" class="section about">
        <div>
          <h2>เกี่ยวกับตัวอย่างนี้</h2>
          <p>
            ตัวอย่างเว็บไซต์นี้สร้างขึ้นด้วยโครงสร้างง่าย ๆ ของ Vue 3 และ Vite เพื่อให้คุณสามารถเริ่มพัฒนาเว็บแอปได้ทันที
          </p>
        </div>
        <div class="about-stats">
          <div>
            <strong>3</strong>
            <span>ส่วนประกอบ</span>
          </div>
          <div>
            <strong>100%</strong>
            <span>Responsive</span>
          </div>
          <div>
            <strong>0</strong>
            <span>ค่าใช้จ่าย</span>
          </div>
        </div>
      </section>

      <section id="contact" class="section contact">
        <div class="contact-card">
          <h2>ติดต่อเรา</h2>
          <p>เริ่มพัฒนาเว็บของคุณได้เลยวันนี้ โดยใช้โค้ดตัวอย่างนี้เป็นพื้นฐาน</p>
          <a class="button primary" href="mailto:hello@example.com">ส่งอีเมลหาเรา</a>
        </div>
      </section>
    </main>

    <footer class="site-footer">
      <p>© 2026 ตัวอย่างเว็บไซต์ — สร้างด้วย Vue 3 และ Vite</p>
    </footer>
  </div>
</template>
