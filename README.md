# Multithread 遊戲
-使用ncurses library實作遊戲介面
-使用multithread 實作遊戲的各種功能

# 遊戲規則:
- 使用上下左右鍵控制飛船
- 星星為背景
- 若碰到小行星則energy減少
- 每隔一段時間若沒有game over則進入下一level(障礙速度加快)
- 當energy使用完或或是使用者輸入’q’遊戲結束
 
# function簡述:
- init() 進行初始化,創建兩個視窗game_wnd和info_wnd,並設置顏色。
- set_level() 每10秒增加一個等級。
- set_pair()根據剩餘能量設置能量條的顏色。
- draw_info()在info_wnd視窗中繪製能量條和等級。
- stars_update() 實現mutex,在game_wnd繪製移動的星星。
- asteroids_update() 實現mutex,在game_wnd繪製移動的小行星。
- player_clr()清除玩家所在位置。
- direction()根據按鍵移動玩家位置。
- game_over_()顯示遊戲結束界面。
- main()主函數,初始化遊戲,創建三個tread。

