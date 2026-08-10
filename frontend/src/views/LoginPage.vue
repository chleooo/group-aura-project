<script setup>
import '../styles/login.css'

const emit = defineEmits(['go-to-create'])
</script>

<template>
  <div class="login-page">
    <section class="login-left-panel">
      <div class="login-dots login-dots-top">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>

      <div class="login-dots login-dots-bottom">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>

      <div class="login-decor book">▱</div>
      <div class="login-decor pencil">✎</div>
      <div class="login-decor document">▤</div>

      <div class="login-curve login-curve-one"></div>
      <div class="login-curve login-curve-two"></div>

      <div class="login-left-content">
        <img
          src="/images/liceo-seal.png"
          alt="Liceo de Cagayan University Seal"
          class="login-seal"
        />

        <h1>
          LICEO<br />
          PEERSHARE
        </h1>

        <div class="login-gold-line"></div>

        <p class="login-description">
          Access your notes, join study groups, and continue learning with your
          Liceo community.
        </p>

        <div class="login-features">
          <div class="login-feature">
            <div class="login-feature-icon">♧</div>
            <h3>Study Smart</h3>
            <p>Find quality materials in one place.</p>
          </div>

          <div class="login-feature">
            <div class="login-feature-icon">♧</div>
            <h3>Stay Connected</h3>
            <p>Keep up with your classmates and groups.</p>
          </div>

          <div class="login-feature">
            <div class="login-feature-icon">♧</div>
            <h3>Grow Faster</h3>
            <p>Learn from shared resources and reviews.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="login-right-panel">
      <div class="login-form-container">
        <div class="login-security-badge">
          <span class="login-badge-icon">♙</span>
          <span>Safe • Student • Liceo</span>
        </div>

        <div class="login-heading">
          <p class="login-welcome">Welcome back <span>👋</span></p>
          <h2>Sign in to your account</h2>
          <p class="login-subtitle">
            Continue where you left off and access your shared study materials.
          </p>
        </div>

        <form @submit.prevent>
          <div class="login-form-group">
            <label>Email Address</label>
            <div class="login-input-wrapper">
              <span class="login-input-icon">✉</span>
              <input type="email" placeholder="Enter your email" />
            </div>
          </div>

          <div class="login-form-group">
            <label>Password</label>
            <div class="login-input-wrapper">
              <span class="login-input-icon">♙</span>
              <input type="password" placeholder="Enter your password" />
              <span class="login-eye">◉</span>
            </div>
          </div>

          <div class="login-options">
            <label class="remember-me">
              <input type="checkbox" />
              <span>Remember me</span>
            </label>
            <a href="#" class="forgot-password">Forgot password?</a>
          </div>

          <button type="submit" class="login-button">
            <span class="login-button-arrow">→</span>
            <span>Sign In</span>
          </button>

          <div class="login-divider">
            <span></span>
            <p>or</p>
            <span></span>
          </div>

          <div class="signup-link">
            <p>New to Liceo PeerShare?</p>
            <button type="button" class="text-link-button" @click="emit('go-to-create')">
              Create Account
            </button>
            <span>→</span>
          </div>
        </form>
      </div>
    </section>
  </div>
</template>
