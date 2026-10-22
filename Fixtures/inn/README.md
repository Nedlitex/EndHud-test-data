# inn

Frames of the inn (缘缘庄, "Yuanyuan's Blazing Stoves") from the owner's two recordings, 3838×2158,
the UID corner (bottom left) blacked out. Read by the inn screen readers (`src/EndHud.Vision/Inn/`).

Table cards: card *n* (1–6) at the top, left edge ≈ 563 + 283·(n−1), about 280 px wide; an order
shows one round picture per item (dish or drink), centred near (left+76, 165) and (left+201, 165).
An item is served when its pip under the number (one per item) is green, or when its picture
carries the blue spinner (a ring of cyan dots: the game serving it automatically). The green smiley
a picture can show means nothing useful and is not read. Card states: empty (number tab only), 点餐中 (grey),
order (white, pictures), 用餐中 (grey, bowl), 待结账 (red), 老饕 (yellow; a gourmand's order shows
category icons instead of pictures).

Dishes and drinks were named by comparing each frame with `inn/pictures.zip` (the table-card
reader's matches agree); timers, cards and meters are as each frame shows them. A card marked
(served) has that item's pip green; (spinner) has the blue auto-serve spinner on it, which counts
as served too.

| File | From | What it shows |
|---|---|---|
| `session-start.jpg` | test_yuanyuan1 154 s | timer 04:57, the HUD still fading in (faint: the timer reads at 4K only, the fire meter not at all); all six tables empty; fire 0/100 |
| `session-fire-0.jpg` | test_yuanyuan1 165 s | the 派单 panel open (kitchen 3), timer 04:46 at the top; T4 点餐中, the rest empty. The fire meter is hidden behind the panel |
| `session-first-order.jpg` | test_yuanyuan1 166.5 s | timer 04:45; T4 点餐中 (its order not out yet), the rest empty; fire 0/100, streak 0 |
| `session-four-orders.jpg` | test_yuanyuan1 205 s | the 派单 panel open (kitchen 1), timer 04:06 at the top. T1 empty; T2 茄果鳞肉汤 (spinner) + 瓶装霞莓饮 (served); T3 empty; T4 白瓜肉丸汤 + 瓶装优质兽奶 (served); T5 麻辣香锅 + 潮前龙井 (served); T6 麻辣香锅 + 瓶装霞莓饮, its card drawn larger (just ordered) |
| `session-gourmand-arrives.jpg` | test_yuanyuan1 217 s | timer 03:54. T1 gourmand 点餐中 (yellow); T2 用餐中; T3 empty; T4 白瓜肉丸汤 + 瓶装优质兽奶 (served); T5 麻辣香锅 (spinner) + 潮前龙井 (served); T6 麻辣香锅 + 瓶装霞莓饮 (served); fire 4/100, streak 2 |
| `session-gourmand-order.jpg` | test_yuanyuan1 220 s | timer 03:51. T1 gourmand order, 2 category icons; T2 用餐中; T3 empty; T4 白瓜肉丸汤 + 瓶装优质兽奶 (served); T5 麻辣香锅 (served) + 潮前龙井 (served); T6 麻辣香锅 + 瓶装霞莓饮 (served); fire 8/100, streak 4. The gourmand's bubble, on four lines: "随便上点，别是滋补药膳 / 那种就行！/ 来点喝的清清口，别是奶 / 味的就行。" |
| `session-gourmand-two-lines.jpg` | owner's live session 2026-10-19, 6:11 | timer 03:27, EndHud's strip at the top right. T4 gourmand order, 2 category icons. The gourmand's bubble, nearer the camera (characters ~55 px), a category icon before each request: "来点汤，要酸口，促消 / 化。/ 上好的肉！做点菜！" (gourmand 5: 汤羹&[酸], 菜肴&<优质肉块>) |
| `session-dispatch-panel.jpg` | test_yuanyuan1 255 s | the 派单 panel: kitchen 3 (赛希 + 伊冯), cook times 金丝小贝 27 s, 雪绵豆沙 20 s, 白瓜肉丸汤 37 s, 勺里游 32 s; 珍馐 chance 18 %; the queue: 金丝小贝 cooking, 1 s left, two empty slots. Timer 03:16. T1 待结账; T2 茄果鳞肉汤 + 潮前龙井 (served); T3 用餐中; T4 empty; T5 gourmand 点餐中; T6 麻辣香锅 + 瓶装霞莓饮 (served) |
| `session-paying-and-waiting.jpg` | test_yuanyuan1 298 s | the 派单 panel open (kitchen 3), timer 02:33 at the top; the cards fully drawn. T1 茄果鳞肉汤 + 瓶装霞莓饮 (served); T2 待结账; T3 老饕; T4 麻辣香锅 + 瓶装霞莓饮 (served); T5 gourmand 用餐中; T6 待结账 |
| `session-gourmand-one-request.jpg` | test_yuanyuan1 301 s | timer 02:30. T1 茄果鳞肉汤 + 瓶装霞莓饮 (served); T2 待结账; T3 老饕; T4 麻辣香锅 + 瓶装霞莓饮 (served); T5 待结账; T6 待结账; fire 61/100, streak 15 |
| `session-two-dishes.jpg` | test_yuanyuan1 313 s | the same moment as session-fire-92 (no two-dish order on screen): timer 02:18. T1 茄果鳞肉汤 (served) + 瓶装霞莓饮 (served); T2 点餐中; T3 gourmand 用餐中; T4 麻辣香锅 + 瓶装霞莓饮 (served); T5 点餐中; T6 待结账; fire 92/100, streak 18 |
| `session-fire-92.jpg` | test_yuanyuan1 313 s | fire 92/100, streak 18 |
| `session-fire-ready.jpg` | test_yuanyuan1 340 s | fire full: the number gone, red button, "开启满堂彩 ▸▸ [R]" (ready, not started); streak 20; timer 01:51. T1 点餐中; T2 金丝小贝 (served) + 麻辣香锅; T3 empty; T4 待结账; T5 金丝小贝 (spinner) + 瓶装霞莓饮 (served); T6 "勺里游" + 金丝小贝 |
| `session-closed.jpg` | test_yuanyuan1 451 s | timer 00:00 in red and the "即将打烊" banner. T1 麻辣香锅 + 潮前龙井 (spinner); T2 empty; T3 白瓜肉丸汤 + 瓶装优质兽奶 (served); T4 用餐中; T5 点餐中; T6 雪绵豆沙 + 麻辣香锅 (served); fire full (ready), streak 36 |
| `setup-theme.jpg` | test_yuanyuan2 42 s | the theme list (//主题设定), 养身心 selected (no stars): objective 开启2次满堂彩, requirement 至少有2道带有[素食]或[滋补]特性的菜品, hot traits 素食 滋补 |
| `setup-chefs-placed.jpg` | test_yuanyuan2 60 s | kitchen 1 大厨佩丽卡 + 大厨艾维文娜, kitchen 2 大厨陈千语, kitchen 3 empty |
| `chef-picker.jpg` | test_yuanyuan2 75 s | 厨房一's chef picker, 2/2 chosen: 大厨佩丽卡 (菜肴, 珍馐; 甜) and 大厨艾维文娜 (菜肴, 甜品; 甜); totals 菜肴 +20 %, 甜品 +10 %, 珍馐 +5 %, 甜 +10 %; the grid of other operators' cards, no names (who they are: below) |
| `setup-soup-entree-empty.jpg` | test_yuanyuan6 55.5 s | 营业设定, theme 一汤一饭 (no stars): text "…客人更倾向主食和汤羹类菜品。", objective 出售20道[主食]类或[汤羹]类的菜品, requirement 至少有2道[主食]类和2道[汤羹]类菜品, hot types 主食 汤羹; Si's 品质把控 5 %; the three kitchens empty (安排干员+), two places each; no EndHud panel yet |
| `chef-picker-kitchen1-empty.jpg` | test_yuanyuan6 61 s | 厨房一's chef picker, 0/2 chosen, hot types 汤羹 主食; EndHud's "厨房一 · 推荐" panel (安塔尔 狼卫; 可换 黎风 洛茜 卡契尔) over the empty bonus list |
| `menu-dishes.jpg` | test_yuanyuan2 66 s | 菜单设定, all dishes tab, 2/8 dishes chosen (白瓜肉丸汤, 莓果甜汤), 0/8 drinks; requirements (Rating 4: ≥3 types, ≥6 dishes and 3 drinks); stock 可烹饪∞ |
| `menu-drinks.jpg` | test_yuanyuan2 96 s | the drinks tab, 8/8 dishes and 0/8 drinks chosen; the eight drinks (瓶装霞莓饮, 潮前龙井, 陈酿葡萄露, 瓶装优质兽奶, 游人酒, 梨花香茶, 瓶装脆蔗汁, 玉米汁); stock 库存∞ |
| `dispatch-panel-queue.jpg` | test_yuanyuan2 108 s | 派单 for 厨房一 (大厨佩丽卡, 大厨艾维文娜), 珍馐 18 %, timer 04:52 at the top; one dish queued, 白瓜肉丸汤 cooking with 40 s left, two empty slots. T1 点餐中, the rest empty |
| `session-fire-meter.jpg` | test_yuanyuan2 141 s | timer 04:25; fire 0/100, streak 0; T1 白瓜肉丸汤 + 瓶装霞莓饮 (served); T2 茄果鳞肉汤 + 果味沙拉 (two dishes); T3 点餐中; T4–T6 empty |
| `session-gourmand-panel.jpg` | owner's live session 2026-10-20 (test_yuanyuan3), 4:26 | timer 02:16, EndHud's banners at the left middle and its gourmand panel at the top right (table 4: 不辣的、不咸的汤羹 + 茶香的). T1 茄果鳞肉汤 + 瓶装霞莓饮 (served); T2 莓果甜汤 + "勺里游"; T3 用餐中; T4 gourmand order, 2 category icons; T5 白瓜肉丸汤 + 瓶装霞莓饮 (served); T6 待结账 |
| `session-hud-faded.jpg` | the same session, 4:29 | the HUD faded out while the camera moves (timer 02:13 faint): no inn screen is found and every table card reads empty, though table 4's gourmand order is still open |
| `dispatch-panel-banners.jpg` | the same session, 4:32 | the 派单 panel for 厨房二, timer 02:10; its cards 至臻鳞肉卷 22 s, 白瓜肉丸汤 23 s, 莓果甜汤 23 s, 果味沙拉 18 s, "勺里游" 20 s, 茄果鳞肉汤 21 s; EndHud's banners over the panel's chef column (厨房二 预做：至臻鳞肉卷 among them). T4 gourmand order |
| `session-gourmand-still-open.jpg` | the same session, 4:35 | timer 02:07, the HUD fading back in; T4 still a gourmand order, EndHud's gourmand panel gone (the bug of 2026-10-20) |
| `menu-soup-theme.jpg` | owner screenshot, 2026-10-19 | 菜单设定 for theme 舌上清流 (4 stars): 4级客栈要求 至少需要3种不同的类型的菜品 / 至少需要6道菜品和3种饮品; 经营主题要求 至少有1道[汤羹]类菜品; 主题热门 汤羹 饮品; 主题加分项 出售10道[汤羹]类菜品; all-dishes tab, 0/8 dishes and 0/8 drinks chosen, stock ∞; no EndHud panel on screen |
| `menu-soup-dessert-theme.jpg` | owner's live session 2026-10-21 (test_yuanyuan4), 0:55 | 菜单设定 for theme 暇时茶点: 4级客栈要求 至少需要3种不同的类型的菜品 / 至少需要6道菜品和3种饮品; 经营主题要求 至少有2道[汤羹]类菜品和2道[甜品]类菜品 (wrapping: its last 品 on a line of its own); 主题热门 汤羹 甜品 茶香 果香; 0/8 dishes and 0/8 drinks; the top of the all-dishes list: 千果珍珠圆, 白瓜肉丸汤, 茄果鳞肉汤, 金丝小贝, 莓果甜汤, 酸辣汤, 雪绵豆沙, 酸莓布丁 (soups and desserts only). EndHud's old menu panel at the bottom left and its "推荐" marks on the cards (the bug of 2026-10-21: two dish types only) |
| `menu-soup-dessert-theme-scrolled.jpg` | the same session, 1:02 | the same screen scrolled a little: 茄果鳞肉汤, 金丝小贝, 莓果甜汤, 酸辣汤, 雪绵豆沙, 酸莓布丁, 豆沙汤圆, 咸酪脆饼, 鲜奶炖蛋 / 糯米凉糕 (cut off) |
| `session-panel-closed-mark-table1.jpg` | the same session, 4:16 | timer 03:12, the 派单 panel CLOSED; EndHud's card mark "排这个（桌1）" left over the dining room (the bug of 2026-10-21) and its two circles for 桌4. T1 酸莓布丁 + drink; T2 用餐中 (yellow); T3, T5, T6 orders; T4 gourmand 点餐中 |
| `session-gourmand-soup-and-drink.jpg` | the same session, 4:20 | timer 03:08. T4 gourmand order, 2 category icons; its bubble, large: "清爽无油的汤羹，有吗？/ 来杯喝的，谨记，我滴酒 / 不沾。" (gourmand 3: 汤羹&非<菜籽油>, 非[酒香]) |
| `session-gourmand-soup-and-drink-far.jpg` | the same session, 4:56 | timer 02:32, the same bubble small and far; EndHud's banners at the left and circles for 桌4 (酸莓布丁, 白瓜肉丸汤: the bug of 2026-10-21) |
| `session-gourmand-soup-and-drink-near.jpg` | the same session, 4:59 | timer 02:29, the same bubble, middle size |
| `session-panel-closed-mark-table2.jpg` | the same session, 5:02 | timer 02:26, the 派单 panel CLOSED; EndHud's card mark "排这个（桌2）" left over table 6; the same bubble, both requests ticked |
| `session-tray-picking-up.jpg` | owner's live session 2026-10-21 (test_yuanyuan5, theme 群鳞会), 200 s | timer 03:07; the tray of held dishes (bottom middle, five slots): 白瓜肉丸汤 (slot selected, white), 福寿全, three empty slots, a yellow arrow over slot 3 (picking up); fire 8/100 |
| `session-panel-just-closed.jpg` | the same session, 252.6 s | timer 02:14 back under the 结束经营 button, the HUD fading in after the 派单 panel closed; EndHud's card mark "预做这个" left over the dining room (the bug of 2026-10-21); tray 至臻鳞肉卷, "勺里游" (珍馐 badge); fire 29/100 |
| `session-tray-two-dishes.jpg` | the same session, 258 s | timer 02:12; tray 至臻鳞肉卷 (selected), "勺里游" (珍馐 badge); EndHud's call "厨房三：至臻鳞肉卷 / 桌4 点的" though one is in hand (the bug of 2026-10-21) |
| `session-tray-one-choice-dish.jpg` | the same session, 300 s | timer 01:27; tray "勺里游" (珍馐 badge, selected), the game's prompt 放回出餐台 (put it back on the counter); fire 66/100 |
| `session-tray-three-dishes.jpg` | the same session, 328 s | timer 00:57; tray "勺里游" (珍馐), 白瓜肉丸汤 (珍馐, selected), 鳞肉水饺 |
| `session-full-blaze-started.jpg` | the same session, 333 s | Full Blaze just started: the meter's button a red circle counting down "01:00", the game's line "赏钱翻倍，速度提升!" left of it, the streak (19) under its red band; EndHud's "开启满堂彩（R）" still up (the bug of 2026-10-21); tray "勺里游" (珍馐), 鳞肉水饺 |
| `session-full-blaze-running.jpg` | the same session, 380 s | timer 00:07, Full Blaze running: the red circle "00:13", the game's line "灶火正旺，满堂生彩!", streak 26; the 即将打烊 banner; tray empty; EndHud's "开启满堂彩（R）" still up |
| `setup-gourmand-theme.jpg` | owner's live session 2026-10-21 (test_yuanyuan8), 0:20 | 营业设定 for theme 食有老饕 (not in inn-data.json): 菜单要求 "至少需要8道菜品和6种饮品 / 且[主食]类、[菜肴]类、[甜品]类、[汤羹]类菜品，每 / 种至少有1道" (a type icon before each bracket); under it the 流行趋势 bar (chip 赏钱, a refresh countdown 13小时39分钟 at its right), 热门类型 汤羹, 热门特性 素食; kitchens empty |
| `menu-gourmand-theme.jpg` | the same session, 2:00 | 菜单设定: 专属菜单要求 "至少需要8道菜品和6种饮品 / 且[主食]类、[菜肴]类、[甜品]类、 / [汤羹]类菜品，每种至少有1道"; 流行趋势 汤羹, 素食 under it; 8/8 dishes and 6/8 drinks; EndHud's menu panel at the bottom left saying it can't read the rule (the bug of 2026-10-21) |

## The chef picker's grid (`chef-picker.jpg`)

Four columns of cards, the card's left edge at x ≈ 109 + 270.5·(c−1) (240 px wide); each card's
dark "暂无安排" bar at y ≈ 545 + 425.5·(r−1). Under the bar, two bonus icons (a gold square with a
bowl = 主食, green = 菜肴, blue = 汤羹, red = 甜品, a yellow circle with a cloche = 珍馐) and the
flavor chip. A fourth row is cut off by the list's bottom edge (not readable). Each card was named
by comparing its portrait with the operator package's wiki avatar (`icons/<id>.png`: the same
drawing, cropped to the head) and checking its icons and flavor against the operator's hobbies and
element; all twelve agree.

| Row | Column 1 | Column 2 | Column 3 | Column 4 |
|---|---|---|---|---|
| 1 | 黎风 (主食 汤羹; 咸) | 莱万汀 (菜肴 珍馐; 辣) | 伊冯 (甜品 甜品; 鲜) | 大潘 (主食 菜肴; 咸) |
| 2 | 秋栗 (主食 主食; 辣) | 卡契尔 (主食 菜肴; 咸) | 埃特拉 (菜肴 珍馐; 鲜) | 萤石 (汤羹 珍馐; 酸) |
| 3 | 安塔尔 (珍馐 珍馐; 甜) | 阿列什 (主食 汤羹; 鲜) | 艾尔黛拉 (菜肴 汤羹; 酸) | 别礼 (主食 珍馐; 鲜) |
| `feast-bubble-short.jpg` | owner's recording 2026-10-21 (test_yuanyuan8, the feast mode: every guest a gourmand of the feast pool), 192.5 s | table 1's gourmand (feast pool 10): its bubble's two requests on a line each, the dish (5 letters) and the drink (3 letters), the drink's icon a green face (served); card 1's second pip green |
| `feast-bubble-wrapped.jpg` | the same session, 204 s | table 2's gourmand (feast 7): each request wraps its last letter onto a line of its own; nothing served yet |
| `feast-bubble-behind-stats.jpg` | the same session, 186 s | table 1's gourmand (feast 10): the session's stats box (income, guests, dishes sold) drawn over the bubble's second line (the drink) |
| `feast-two-bubbles.jpg` | the same session, 359.5 s | two bubbles: table 4's gourmand (feast 11, the vegetable-mushroom dish and an alcohol-free drink) near, table 6's (feast 14) far and smaller; a third, small bubble with the hand-raised icon (table 4's next guest waiting) |
| `feast-bubble-faces.jpg` | the same session, 365 s | table 6's gourmand (feast 14): both requests' icons red faces (failed); card 6's pips red |
| `feast-two-soups.jpg` | the same session, 406 s | table 5's gourmand (feast 4): two soup requests, a dish icon before each |
| `feast-two-bubbles-one-resolved.jpg` | the same session, 401 s | table 2's gourmand (feast 10, drink a green face) and table 4's far (feast 11, dish a red face) |
| `feast-cards-pips.jpg` | the same session, 231 s | the cards: tables 1 and 2 gourmand orders with the second pip green (drink served), table 4 gourmand ordering, table 5 gourmand order with the first pip red (dish failed), tables 3 and 6 empty; table 5's bubble behind the stats box |
