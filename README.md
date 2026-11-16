:root {
  font-family: Inter, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  line-height: 1.5;
  font-weight: 400;
  color: #f5f7ff;
  background: #07111f;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

* {
  box-sizing: border-box;
}

html, body, #app {
  margin: 0;
  min-height: 100%;
  min-height: 100vh;
}

body {
  background:
    radial-gradient(circle at top, rgba(126, 87, 194, 0.35), transparent 30%),
    linear-gradient(145deg, #06111c 0%, #0d1d2d 38%, #0a1320 100%);
}

button, input {
  font: inherit;
}

button {
  cursor: pointer;
}

.app-shell {
  min-height: 100vh;
  display: grid;
  place-items: center;
  padding: 24px;
}

.lock-screen {
  width: 100%;
  display: flex;
  justify-content: center;
}

.lock-card {
  width: min(100%, 420px);
  background: rgba(10, 16, 29, 0.82);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 0 25px 80px rgba(0, 0, 0, 0.45);
  border-radius: 26px;
  padding: 32px 26px;
  display: flex;
  flex-direction: column;
  gap: 14px;
  backdrop-filter: blur(14px);
}

.brand-row {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  margin-bottom: 4px;
}

.brand-mark {
  font-size: 1.8rem;
}

.lock-card h1,
.topbar h2 {
  margin: 0;
  font-weight: 700;
}

.lock-subtitle {
  color: rgba(255, 255, 255, 0.72);
  margin: 0 0 8px;
  text-align: center;
}

.lock-card input {
  width: 100%;
  border: 1px solid rgba(255, 255, 255, 0.12);
  background: rgba(255, 255, 255, 0.04);
  color: #f6f8ff;
  padding: 14px 16px;
  border-radius: 12px;
  outline: none;
}

.lock-card input:focus {
  border-color: rgba(138, 92, 246, 0.9);
  box-shadow: 0 0 0 3px rgba(138, 92, 246, 0.2);
}

.lock-card button,
.ghost-button,
.upload-button,
.card-footer button,
.modal-meta button {
  border: none;
  border-radius: 12px;
  color: white;
  font-weight: 600;
  transition: transform 0.2s ease, opacity 0.2s ease;
}

.lock-card button,
.upload-button {
  background: linear-gradient(135deg, #8b5cf6, #4f46e5);
  padding: 12px 16px;
}

.ghost-button,
.card-footer button,
.modal-meta button {
  background: rgba(255, 255, 255, 0.07);
  padding: 10px 12px;
}

.lock-card button:hover,
.ghost-button:hover,
.upload-button:hover,
.card-footer button:hover,
.modal-meta button:hover {
  transform: translateY(-1px);
  opacity: 0.95;
}

.gallery-page {
  width: min(1200px, 100%);
  min-height: 100vh;
  padding: 40px 20px 60px;
}

.topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  margin-bottom: 26px;
}

.eyebrow {
  margin: 0;
  font-size: 0.8rem;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: #9cb5ff;
}

.header-actions {
  display: flex;
  gap: 10px;
  align-items: center;
  flex-wrap: wrap;
}

.upload-button {
  position: relative;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.upload-button input {
  position: absolute;
  inset: 0;
  opacity: 0;
  cursor: pointer;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 18px;
}

.gallery-card {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.09);
  border-radius: 18px;
  overflow: hidden;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.18);
}

.gallery-card img {
  width: 100%;
  height: 260px;
  display: block;
  object-fit: cover;
  cursor: pointer;
}

.card-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  padding: 12px 14px 14px;
}

.card-footer span {
  color: rgba(255, 255, 255, 0.84);
  font-size: 0.96rem;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.modal-backdrop {
  position: fixed;
  inset: 0;
  display: grid;
  place-items: center;
  background: rgba(4, 10, 18, 0.78);
  padding: 24px;
}

.modal {
  width: min(900px, 100%);
  background: rgba(10, 15, 22, 0.94);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 20px;
  overflow: hidden;
}

.modal img {
  display: block;
  width: 100%;
  max-height: 72vh;
  object-fit: contain;
  background: #02070c;
}

.modal-meta {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
  padding: 16px 18px;
}

.modal-meta h3 {
  margin: 0;
}

@media (max-width: 640px) {
  .topbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .header-actions {
    width: 100%;
  }

  .header-actions > * {
    flex: 1 1 100%;
  }

  .modal-meta {
    flex-direction: column;
    align-items: flex-start;
  }
}
