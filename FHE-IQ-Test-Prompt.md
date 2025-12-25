# PROMPT: Tạo dApp FHE IQ Test - "Big Brain or Smooth Brain?"

## 🎯 Tổng Quan
Tạo một dApp (Decentralized Application) đánh giá IQ vui nhộn, kết hợp:
- Fully Homomorphic Encryption (FHE) để mã hóa câu trả lời
- Kết nối ví Web3 (MetaMask)
- Meme culture và âm thanh viral
- UI/UX cyberpunk, neon, gaming style

---

## 📋 YÊU CẦU CHI TIẾT

### 1. CÔNG NGHỆ
- Single HTML file với React (CDN)
- Inline CSS với animations
- Web Audio API cho sound effects
- Không cần backend, chạy offline được

### 2. MÀN HÌNH (5 screens)

#### Screen 1: WELCOME
- Logo brain emoji 🧠 với animation float/pulse
- Title "FHE IQ TEST" với gradient text rainbow animation
- Subtitle: "Big Brain or Smooth Brain?"
- Tags: 🔐 FHE Encrypted, 👛 Web3, 🎭 Meme-fied, 🔊 Sounds
- Button "CONNECT WALLET" với shimmer effect
- Info: "10 câu hỏi • 25s/câu"

#### Screen 2: CONNECTING
- Wallet emoji 👛 bouncing
- Text "Đang kết nối ví..." với loading dots
- Generate mock wallet address (0x...)

#### Screen 3: QUIZ
- Header bar:
  - Wallet avatar + address (truncated)
  - Progress: "Câu X/10" + progress bar
  - Score: "⭐ X pts"
  - Timer: "⏱️ Xs" (đỏ + shake khi ≤10s)
  
- Question card:
  - Badge loại câu hỏi (🧠 IQ / 🎭 TRICK / 🐸 MEME)
  - Badge điểm (+X pts)
  - Câu hỏi text
  - 4 options dạng button grid 2x2
  - Hover effect: purple glow, translateY(-4px)
  
- Khi trả lời:
  - Đúng: option xanh + particles confetti + sound correct
  - Sai: option đỏ + particles sad + sound wrong
  - Hiện explanation box với giải thích
  - Button "CÂU TIẾP →" hoặc "🎉 XEM KẾT QUẢ"

#### Screen 4: COMPUTING (FHE Animation)
- Icon 🔐 pulse ở giữa
- 4 vòng tròn expanding animation (ring effect)
- Text steps:
  1. "Mã hóa câu trả lời..."
  2. "Tạo FHE ciphertext..."
  3. "Homomorphic computation..."
  4. "Tính toán IQ..."
  5. "Giải mã kết quả..."
- Progress bar 5 steps

#### Screen 5: RESULT
- Emoji lớn theo level IQ
- Title + Subtitle meme
- IQ Score lớn với glow effect
- Description text
- Stats box: Điểm, Số đúng, Tỉ lệ %
- Buttons: Mint NFT, Share Twitter, Test Lại

---

### 3. CÂU HỎI (18 câu, random 10)

#### IQ Chuẩn (8 câu):
```
1. Dãy số: 2, 6, 12, 20, 30, ? → 42 (n²+n)
2. Logic: Zorp-Morp-Dorp → Đúng (subset logic)
3. So sánh: A>B, C<B, D>A → C chậm nhất
4. Ngày: ngày mai là ngày kia của hôm qua → Thứ Ba
5. Phân số: 1/2 × 2/3 × 3/4 × 4/5 × 100 → 20
6. Fibonacci: 1,1,2,3,5,8,13,? → 21
7. Đốt gì trước: đèn/nến/lò sưởi → Que diêm
8. Look-and-say: 1,11,21,1211,111221,? → 312211
```

#### Trick Questions (8 câu):
```
1. Bao nhiêu tháng có 28 ngày? → 12 (tất cả)
2. Có 3 táo, lấy đi 2 → Có 2 (bạn lấy)
3. Từ viết SAI trong từ điển → "Wrong"
4. Gà hay trứng trước? → Trứng (tiến hóa)
5. "Câu này là SAI" → Paradox
6. Cha của con bạn là ai? → Chính bạn
7. Nhà hướng Nam, gấu màu gì? → Trắng (Bắc Cực)
8. Chôn người sống sót ở đâu? → Không chôn!
```

#### Meme Questions (2 câu):
```
1. Two Buttons meme → Cả hai đều đúng/sai
2. Doge speak không phải → "So intellectual"
```

**Format câu hỏi:**
```javascript
{
  id: number,
  type: 'standard' | 'trick' | 'meme',
  question: string (có emoji),
  options: string[4],
  correct: 0-3,
  points: 5-25,
  explanation: string
}
```

---

### 4. HỆ THỐNG ĐIỂM

| Loại | Điểm |
|------|------|
| IQ Easy | 5 |
| IQ Medium | 10 |
| IQ Hard | 15 |
| Trick | 15-25 |
| Meme | 8-10 |

**Công thức IQ:**
```
IQ = 70 + (score / maxScore) × 100
```

---

### 5. KẾT QUẢ MEME (7 levels)

| IQ | Emoji | Title | Subtitle |
|----|-------|-------|----------|
| 0-70 | 🧠💨 | SMOOTH BRAIN | "Average Crypto Investor" |
| 71-90 | 🐕 | DOGE BRAIN | "Such Smart. Much Wow." |
| 91-105 | 🤖 | NPC MODE | "Quest accepted" |
| 106-120 | 🧐 | HMMMM... | "Shallow and Pedantic" |
| 121-140 | 🦍 | RETURN TO MONKE | "Reject Modernity" |
| 141-160 | 🌌 | GALAXY BRAIN | "You See The Matrix" |
| 161+ | 👁️ | ILLUMINATI | "Too Powerful" |

Mỗi level có:
- Emoji đặc trưng
- Title + Subtitle meme
- Description text vui
- Color riêng

---

### 6. ÂM THANH (Web Audio API)

Tạo SoundManager với các method:
```javascript
playCorrect()  // 3 notes ascending: C5-E5-G5
playWrong()    // 2 notes descending sawtooth
playClick()    // Short blip
playConnect()  // 4 notes melody (Windows style)
playVictory()  // Happy melody 9 notes
playDefeat()   // Sad descending 5 notes
playTick()     // Timer tick khi ≤5s
playTimeout()  // Long low sawtooth
```

Dùng OscillatorNode + GainNode, exponentialRampToValueAtTime cho fade out.

---

### 7. ANIMATIONS

```css
@keyframes gradient    // Background gradient moving
@keyframes float       // Logo floating up-down
@keyframes pulse       // Scale 1 → 1.1 → 1
@keyframes shake       // Left-right shake (timer warning)
@keyframes shimmer     // Button shine effect
@keyframes ring        // Expanding circles (FHE)
@keyframes rise        // Particles flying up + fade
@keyframes rainbow     // Text color cycling
@keyframes correctPulse // Scale bump on correct
@keyframes wrongShake   // Horizontal shake on wrong
```

---

### 8. UI/UX STYLE

**Color Palette:**
- Background: #0f0f1a → #1a1a2e → #16213e (gradient)
- Primary: #A855F7 (Purple)
- Secondary: #4ECDC4 (Cyan/Teal)
- Accent: #FFE66D (Yellow)
- Error: #FF6B6B (Coral)
- Text: #fff, #888, #666

**Typography:**
- Title: 'Press Start 2P' (retro gaming)
- Body: 'Space Mono' (tech monospace)
- Fun text: 'Comic Neue'

**Effects:**
- Backdrop blur trên cards
- Box shadows với màu glow
- Gradient borders
- Neon text shadows
- Grid pattern background
- Radial gradient spots

---

### 9. COMPONENTS STRUCTURE

```
FHEIQTestApp
├── State: screen, wallet, currentQ, answers, score, iq, time...
├── Effects: timer, sound init, questions shuffle
├── Functions: connect, handleAnswer, handleTimeout, next, compute, reset
├── Render:
│   ├── Particles layer
│   ├── Sound toggle button
│   ├── FHE badge (bottom-left)
│   └── Screen content (switch by state)
```

---

### 10. TÍNH NĂNG BỔ SUNG

- [ ] Sound toggle button (top-right)
- [ ] FHE badge "🔐 FHE Encrypted • Zama fhEVM" (bottom-left)
- [ ] Responsive design (mobile-friendly)
- [ ] Particles effect khi đúng/sai (20-30 emojis bay lên)
- [ ] Progress bar gradient
- [ ] Hover effects trên tất cả buttons
- [ ] Smooth transitions giữa screens

---

## 🚀 OUTPUT

Tạo **1 file HTML duy nhất** chứa:
- React + ReactDOM từ CDN
- Babel standalone để compile JSX
- Google Fonts link
- Tất cả CSS inline trong component
- Tất cả logic trong 1 component FHEIQTestApp
- Có thể mở trực tiếp bằng browser, không cần server

---

## 💡 GỢI Ý IMPLEMENTATION

1. Bắt đầu với state management đơn giản (useState)
2. Tạo SoundManager object riêng với Web Audio API
3. CSS-in-JS style (inline styles object)
4. Shuffle questions với sort(() => Math.random() - 0.5)
5. Timer dùng setInterval trong useEffect
6. Particles: tạo array objects {id, x, y, emoji, delay}, render với position fixed
7. Mock wallet: generate random hex string

---

## ✅ CHECKLIST

- [ ] 5 màn hình hoạt động đúng flow
- [ ] 18 câu hỏi với đáp án và giải thích
- [ ] Timer countdown 25s
- [ ] Âm thanh cho các events
- [ ] 7 levels kết quả meme
- [ ] Particles animation
- [ ] Responsive trên mobile
- [ ] Có thể chơi offline

---

**END OF PROMPT**
