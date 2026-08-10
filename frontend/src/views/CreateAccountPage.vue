<script setup>
import '../styles/create-account.css'

const emit = defineEmits(['go-to-login'])
</script>

<template>
  <div class="create-account-page">
    <section class="left-panel">
      <div class="dots dots-top">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>

      <div class="dots dots-bottom">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>

      <div class="decor-icon book-icon">▱</div>
      <div class="decor-icon pencil-icon">✎</div>
      <div class="decor-icon document-icon">▤</div>

      <div class="curve curve-one"></div>
      <div class="curve curve-two"></div>

      <div class="left-content">
        <img
          src="/images/liceo-seal.png"
          alt="Liceo de Cagayan University Seal"
          class="liceo-seal"
        />

        <h1>
          LICEO<br />
          PEERSHARE
        </h1>

        <div class="gold-line"></div>

        <p class="brand-description">
          The official collaborative hub for Liceo students to share notes,
          reviewers, and study guides.
        </p>

        <div class="features">
          <div class="feature">
            <div class="feature-icon">♧</div>
            <h3>Share Notes</h3>
            <p>Upload and access<br />study materials.</p>
          </div>

          <div class="feature">
            <div class="feature-icon">♧</div>
            <h3>Connect</h3>
            <p>Collaborate with<br />fellow students.</p>
          </div>

          <div class="feature">
            <div class="feature-icon">♧</div>
            <h3>Succeed</h3>
            <p>Learn together,<br />grow together.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="right-panel">
      <div class="form-container">
        <div class="security-badge">
          <span class="badge-icon">♙</span>
          <span>Safe • Student • Liceo</span>
        </div>

        <div class="form-heading">
          <h2>Create your account</h2>
          <p>Join the Liceo student resources community</p>
        </div>

        <form @submit.prevent>
          <div class="form-row">
            <div class="form-group">
              <label>First Name</label>
              <div class="input-wrapper">
                <span class="input-icon">♙</span>
                <input type="text" placeholder="First Name" />
              </div>
            </div>

            <div class="form-group">
              <label>Last Name</label>
              <div class="input-wrapper">
                <span class="input-icon">♙</span>
                <input type="text" placeholder="Last Name" />
              </div>
            </div>
          </div>

          <div class="form-row">
            <div class="form-group">
              <label>Liceo Email</label>
              <div class="input-wrapper">
                <span class="input-icon">✉</span>
                <input type="email" placeholder="user@liceo.edu.ph" />
              </div>
            </div>

            <div class="form-group">
              <label>Student ID</label>
              <div class="input-wrapper">
                <span class="input-icon">▣</span>
                <input type="text" placeholder="e.g. 0123456789" />
              </div>
            </div>
          </div>

          <div class="form-row">
            <div class="form-group">
              <label>Course / Department</label>
              <div class="input-wrapper">
                <span class="input-icon">♢</span>
                <select>
                  <option value="">BS Computer Science</option>
                  <option>BS Information Technology</option>
                  <option>BS Information Systems</option>
                  <option>BS Computer Engineering</option>
                </select>
                <span class="dropdown-arrow">˅</span>
              </div>
            </div>

            <div class="form-group">
              <label>Year Level</label>
              <div class="input-wrapper">
                <span class="input-icon">▥</span>
                <select>
                  <option value="">Year Level</option>
                  <option>1st Year</option>
                  <option>2nd Year</option>
                  <option>3rd Year</option>
                  <option>4th Year</option>
                </select>
                <span class="dropdown-arrow">˅</span>
              </div>
            </div>
          </div>

          <div class="form-row">
            <div class="form-group">
              <label>Password</label>
              <div class="input-wrapper">
                <span class="input-icon">♙</span>
                <input type="password" placeholder="Create a strong password" />
                <span class="eye-icon">◉</span>
              </div>
            </div>

            <div class="form-group">
              <label>Confirm Password</label>
              <div class="input-wrapper">
                <span class="input-icon">♙</span>
                <input type="password" placeholder="Repeat your password" />
                <span class="eye-icon">◉</span>
              </div>
            </div>
          </div>

          <div class="terms">
            <input type="checkbox" id="terms" />
            <label for="terms">
              I agree to the
              <span>Terms of Use</span>
              and
              <span>Privacy Policy</span>
            </label>
          </div>

          <button type="submit" class="create-button">
            <span>Create Account</span>
            <span class="button-arrow">→</span>
          </button>

          <div class="divider">
            <span></span>
            <p>or</p>
            <span></span>
          </div>

          <div class="login-link">
            <p>Already have an account?</p>
            <button type="button" class="text-link-button" @click="emit('go-to-login')">
              Sign In
            </button>
            <span>→</span>
          </div>
        </form>
      </div>
    </section>
  </div>
</template>
