# inn

Frames of the inn (缘缘庄, "Yuanyuan's Blazing Stoves") from the owner's two recordings, 3838×2158,
the UID corner (bottom left) blacked out. Read by the inn screen readers (`src/EndHud.Vision/Inn/`).

Table cards: card *n* (1–6) at the top, left edge ≈ 563 + 283·(n−1), about 280 px wide; an order
shows one round picture per item (dish or drink), centred near (left+76, 165) and (left+201, 165).
On a picture, a cyan flower = being made, a green smiley = ready; the pips under the number (one
per item) turn green as each item is served. Card states: empty (number tab only), 点餐中 (grey),
order (white, pictures), 用餐中 (grey, bowl), 待结账 (red), 老饕 (yellow; a gourmand's order shows
category icons instead of pictures).

Items marked *to label* are left for whoever writes the reader to fill in after comparing the
frame with `inn/pictures.zip`, never guessed.

| File | From | What it shows |
|---|---|---|
| `session-start.jpg` | test_yuanyuan1 154 s | timer 04:56; all six tables empty; fire 0/100 |
| `session-fire-0.jpg` | test_yuanyuan1 165 s | fire meter 0/100, streak 0 (right side); T4 点餐中 or its first order |
| `session-first-order.jpg` | test_yuanyuan1 166.5 s | first order: T4 白瓜肉丸汤 + 瓶装优质兽奶; the rest empty |
| `session-four-orders.jpg` | test_yuanyuan1 205 s | timer 04:05. T1 empty; T2 茄果鳞肉汤 (being made) + 瓶装霞莓饮 (ready); T3 empty; T4 白瓜肉丸汤 + 瓶装优质兽奶 (ready); T5 麻辣香锅 + 潮前龙井 (ready); T6 麻辣香锅 + 瓶装霞莓饮 |
| `session-gourmand-arrives.jpg` | test_yuanyuan1 217 s | timer 03:53. T1 老饕 (yellow); T2 用餐中; T3 empty; T4–T6 orders as above |
| `session-gourmand-order.jpg` | test_yuanyuan1 220 s | timer 03:50. T1 gourmand order, 2 category icons; T2 待结账; T3 点餐中; T4 order; T5 用餐中; T6 order |
| `session-dispatch-panel.jpg` | test_yuanyuan1 255 s | the 派单 panel: kitchen 3 (赛希 + 伊冯), cook times 金丝小贝 27 s, 雪绵豆沙 20 s, 白瓜肉丸汤 37 s, 勺里游 32 s; 珍馐 chance 18 % |
| `session-paying-and-waiting.jpg` | test_yuanyuan1 298 s | timer 02:32; the HUD mid-fade (cards translucent): a reader may say "can't read" here. T1 order; T2 待结账; T3 老饕; T4 order; T5 gourmand 用餐中; T6 待结账 |
| `session-gourmand-one-request.jpg` | test_yuanyuan1 301 s | timer 02:29. T1 order (*to label*); T2 empty; T3 gourmand order, 1 category icon; T4 order (*to label*); T5 待结账; T6 待结账; fire 61/100 |
| `session-two-dishes.jpg` | test_yuanyuan1 313 s | timer 02:17. T1 用餐中; T2 two dishes, no drink (*to label*); T3 gourmand 用餐中; T4 order (*to label*); T5 点餐中; T6 待结账; fire 92/100 |
| `session-fire-92.jpg` | test_yuanyuan1 313 s | fire 92/100, streak 18 |
| `session-fire-ready.jpg` | test_yuanyuan1 340 s | fire full: the number gone, red button, "开启满堂彩 ▸▸ [R]" (ready, not started) |
| `session-closed.jpg` | test_yuanyuan1 451 s | timer 00:00 and "已打烊，新客不再进入". T1 order (*to label*); T2 empty; T3 order; T4 用餐中; T5 点餐中; T6 order (*to label*) |
| `setup-theme.jpg` | test_yuanyuan2 42 s | 营业设定: theme 养身心 (no stars), objective 开启2次满堂彩, requirement 至少有2道带有[素食]或[滋补]特性的菜品, hot traits 素食 滋补; 3 kitchens, no chefs |
| `setup-chefs-placed.jpg` | test_yuanyuan2 60 s | kitchen 1 大厨佩丽卡 + 大厨艾维文娜, kitchen 2 大厨陈千语, kitchen 3 empty |
| `chef-picker.jpg` | test_yuanyuan2 75 s | 厨房一's chef picker, 2/2 chosen: 大厨佩丽卡 (菜肴, 珍馐; 甜) and 大厨艾维文娜 (菜肴, 甜品; 甜); totals 菜肴 +20 %, 甜品 +10 %, 珍馐 +5 %, 甜 +10 %; the grid of other operators' cards, no names |
| `menu-dishes.jpg` | test_yuanyuan2 66 s | 菜单设定, all dishes tab, 3/8 chosen; requirements (Rating 4: ≥3 types, ≥6 dishes and 3 drinks); stock 可烹饪∞ |
| `menu-drinks.jpg` | test_yuanyuan2 96 s | the drinks tab, 8/8 dishes and 2/8 drinks chosen (瓶装霞莓饮, 陈酿葡萄露 highlighted); stock 库存∞ |
| `dispatch-panel-queue.jpg` | test_yuanyuan2 108 s | 派单 for 厨房一 (大厨佩丽卡, 大厨艾维文娜), 珍馐 18 %, a full queue of three (*to label*; the last 38 s), every slot with its "−" |
| `session-fire-meter.jpg` | test_yuanyuan2 141 s | timer 04:23; fire 0/100; T1 order, T2 order, T3 点餐中 (*to label*) |
