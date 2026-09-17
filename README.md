# 戰國·第六天魔王 — Web UAT Build

由 GitHub main repo（`alphakey-marketing/sengoku-remake`）匯出嘅 Godot 4.7.2 HTML5 build。

## 點樣重新 build（Windows）
```bash
# 1) export template 已裝喺 %APPDATA%/Godot/export_templates/4.7.2.stable/
cd D:/Download/Sengoku
./godot/Godot_v4.7.2-stable_win64_console.exe --headless --path godot_game --export-release "Web" "D:/Download/Sengoku/build/index"
# 2) 代換 index.html 嘅 $GODOT_* tokens（headless 唔會代）→ 見 build_html_patch.py
# 3) git add && push → Pages 自動更新
```

## Notes
- `user://` save = 瀏覽器 IndexedDB（每個 browser 獨立）
- 字型 = Noto Sans TC（OFL 自由授權）
- 原始碼/素材喺 private repo；呢度淨係放 build 產物
