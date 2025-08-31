# 🚀 Google Summer of Code 2025 – Final Submission  

**Organization**: [Rocket.Chat](https://github.com/RocketChat)  
**Project**: E2E Testing using Maestro  
**Student**: **Rohit Bansal**  
**Mentor**: **Diego Mello**  

---

## 📖 About the Project  

Rocket.Chat is a **leading open-source communication platform** trusted by millions worldwide.  
To ensure a smooth experience, reliable **end-to-end testing** and **seamless release pipelines** are critical.  

Previously, Rocket.Chat relied on **Detox** for E2E testing. While powerful, it posed challenges with **maintainability** and **onboarding new contributors**.  

During **Google Summer of Code 2025**, I set out to improve this by:  

✨ Replacing Detox with **Maestro**, a stable E2E testing framework  
✨ Converting all **test flows** from Detox to Maestro  
✨ Integrating Maestro into **GitHub Actions** for Android & iOS CI runs  
✨ Writing **contributor documentation** so developers can run tests locally  
✨ Migrating **release automation** from CircleCI → GitHub Actions  

This work ensures Rocket.Chat mobile apps are **easier to test, faster to release, and more contributor-friendly**.  

---

## 💡 Key Contributions  

### 🔹 End-to-End Testing (Maestro)  
| PR | Status | Description |
|----|--------|-------------| 
| [#6500](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6500) | ✅ Merged | Base setup for Maestro and migrated onboarding |
| [#6561](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6561) | ✅ Merged | Team coverage for Maestro |
| [#6575](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6575) | ✅ Merged | More team coverage |
| [#6588](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6588) | ✅ Merged | Update create account test script to support UI changes |
| [#6590](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6590) | ✅ Merged | Improvements to handle Android emulator & iOS simulator errors |
| [#6599](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6599) | ✅ Merged | Upgrade Maestro to version 2 |
| [#6593](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6593) | 🔄 Open | Migrate create room test |
| [#6598](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6598) | 🔄 Open | Migrate room test |
| [#6606](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6606) | 🔄 Open | Migrate share-message and ignore-user test |
| [#6576](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6576) | 🛠️ In Progress | Reducing E2E build time by ~70% |

---

### 🔹 CI/CD Release Automation  
| PR | Description |
|----|-------------|
| [#6418](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6418) | Migrate lint and Jest testing from CircleCI → GitHub Actions |
| [#6447](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6447) | Build and release automation using GitHub Actions |
| [#6495](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6495) | Improvements to GitHub build actions |
| [#6517](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6517) | Fix iOS build and version issues |
| [#6571](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6571) | Improved build version logic with repo variables |
| [#6577](https://github.com/RocketChat/Rocket.Chat.ReactNative/pull/6577) | Optimized iOS build by configuring Fastlane for GitHub Action environment |

---

## 🛣️ Milestones  

✅ Setup Maestro in Rocket.Chat React Native repo  
✅ Migrate onboarding tests  
✅ Migrate team tests  
⬜ Migrate room tests  
⬜ Migrate assorted tests  
✅ Integrate flows into GitHub Actions CI  
✅ Add contributor documentation  
✅ Migrate Fastlane release automation → GitHub Actions  
⬜ Improve the build time for E2E build  
⬜ Run tests on multiple OS versions to ensure app stability  

---

## ⚠️ Challenges Faced & Ongoing Work  

While making progress, I also encountered challenges that I am actively addressing:  

1. **Build Times**  
   - Issue: Even with caching, iOS builds on GitHub Actions (macOS-15 runners) take longer than average.  
   - Status: On Android, I optimized the pipeline to achieve **~7 mins build time** (PR pending merge). I am exploring similar improvements for iOS.  

2. **iOS Simulator Stability**  
   - Issue: On macOS-15 GitHub runners, iOS simulators fail to start the tests **~90% of the time** due to slowness.  
   - Status: Working on strategies to improve reliability.

These challenges are ongoing, and I plan to continue improving them beyond GSoC to make the testing pipeline even more reliable.  

---

## 🔮 Future Scope

1. **Expand Test Coverage** – Continue covering the remaining parts of the app with E2E tests.  
2. **Add More Tests** – Introduce additional test scenarios to improve reliability.  
3. **Matrix Strategy** – Run tests across multiple OS versions for broader compatibility.  
4. **Multi-Device Testing** – Execute tests on multiple devices in parallel to further reduce runtime.  
5. **Build Optimization** – Continue refining both iOS and Android build times.  
6. **Smarter Notifications** – Notify contributors directly in PRs when a test fails, including recordings and screenshots for quick fixes.  
7. **Deployment Alerts** – Notify maintainers when a development build fails to deploy, improving visibility and faster recovery.  

---

✨ With this work, Rocket.Chat’s mobile app testing and release pipeline is now more **robust, scalable, and contributor-friendly** — paving the way for faster innovation and higher quality releases.
