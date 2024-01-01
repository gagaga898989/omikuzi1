import sys
import tkinter as tk
from tkinter import messagebox
import random
root = tk.Tk()

root.title("新春おみくじ")
root.geometry("800x700")

# 画像の取得
kuji_img_path = [
        tk.PhotoImage(file = "omikuji_daikichi.png"),
        tk.PhotoImage(file = "omikuji_chuukichi.png"),
        tk.PhotoImage(file = "omikuji_syoukichi.png"),
        tk.PhotoImage(file = "omikuji_kichi.png"),
        tk.PhotoImage(file = "omikuji_suekichi.png"),
        tk.PhotoImage(file = "omikuji_daikyou.png"),
    ]

# 画像切替
def push1():
    fortunes = ["大吉", "中吉", "小吉", "吉", "末吉", "大凶"]
    res = random.randint(0,5)
    label1.configure(image=kuji_img_path[res])
    messagebox.showinfo('結果', f'{EditBox.get()}の運勢は{fortunes[res]}')
    if res == 0:
        button.place(x=400, y=550)
    if res == 5:
        button2.place(x=300, y=550)

def my_daikiti():
    messagebox.showinfo('おめでとう！', '今年は最高の一年になるでしょう')
def my_kyou():
    messagebox.showinfo('厄払い', 'くじを結びました')

# ボタン
Button1 = tk.Button(text='おみくじを引く',fg='red', width=50,command = push1)
Button1.place(x=220, y=510)

button = tk.Button(text="大吉を引いたあなたへ",command=my_daikiti)
button2 = tk.Button(text="くじを結ぶ",command=my_kyou)

# ラベル
#label1 = tk.Label(root,image=random.choice(kuji_img_path))
label1 = tk.Label(root,image=tk.PhotoImage(file="syougatsu2_omijikuji3.png"))
label1.place(x=600, y=200)

# キャンバス作成
canvas = tk.Canvas(bg="white", height=400, width=500)
# キャンバス表示
canvas.place(x=50, y=30)
# イメージ作成
img = tk.PhotoImage(file="omikuji-torii.png", height=400, width=500)
# キャンバスにイメージを表示
canvas.create_image(30, 30, image=img, anchor=tk.NW)

l = tk.Label(
    text=('新年の運試しおみくじ'), 
    font=("",20)#表示文字
    )
l.pack()
l2 = tk.Label(
    text=('使用：フリーイラスト素材集 ジャパクリップ'),   #表示文字
    )
l2.place(x=500, y=600)
l6 = tk.Label(
    text=('イラストや'),   #表示文字
    )
l6.place(x=540, y=620)
l3 = tk.Label(
    text=('名前を入力してください:'),   #表示文字
    )
l3.place(x=250, y=450)
l4 = tk.Label(
    text=('↓結果↓'),   #表示文字
    )
l4.place(x=600, y=150)
EditBox = tk.Entry(width=100)
EditBox = tk.Entry()
EditBox.insert(tk.END,"名無しのごんべえ")
EditBox.place(x=400, y=450)



# ループ
root.mainloop()
