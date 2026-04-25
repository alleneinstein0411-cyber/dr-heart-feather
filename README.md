# 張醫師心羽診間

用診間故事，陪民眾看懂心臟病、心導管與治療選擇。

這是一個 Astro + Markdown 的靜態衛教網站，適合部署到 GitHub Pages，再用 Cloudflare 管理自訂網域。

## 常用指令

```sh
npm install
npm run dev
npm run build
npm run preview
```

## 寫新文章

文章放在 `src/content/blog/`。每篇文章是一個 Markdown 檔，frontmatter 建議保留這些欄位：

```md
---
title: "文章標題"
description: "給列表與 SEO 使用的一句話摘要"
category: "症狀"
tags: ["胸悶", "心導管"]
sourceLevel: "快速衛教文"
pubDate: "2026-04-25"
---
```

## GitHub Pages

這個 repo 已經附上 `.github/workflows/deploy.yml`。推到 GitHub 之後，到 repository settings 的 Pages 頁面，Source 選 `GitHub Actions`。

目前 `astro.config.mjs` 的 `base` 設為 `/dr-heart-feather`，這是為了讓 GitHub project site 的臨時網址能正常運作。

若之後買了自訂網域，在 GitHub Pages 裡填入網域，並到 Cloudflare 設定 DNS 指向 GitHub Pages。自訂網域生效後，請把 `astro.config.mjs` 的 `site` 改成正式網域，並移除 `base`。

## 醫療內容提醒

本站文章供衛教參考，不能取代實際診療。個案故事需匿名化與改寫，不放可識別病人資訊，也不使用保證療效或過度招徠的文字。
