# lern-gitnub

import tkinter as tk
import webbrowser
import buttonweb as BW
import buttonmap as BM
import pygame
from tkinter import ttk
from PIL import Image, ImageTk

def Out_A4a():
    message_A4a = userInput.get()
    print(message_A4a)  

def button_frame(frame):
    notebook.select(frame)

def button_A1():
    button_frame(frame_A1)
    pygame.mixer.init()
    pygame.mixer.music.stop()
    pygame.mixer.music.load('D:/งาน/project/GUIS/speak/button1.mp3')
    pygame.mixer.music.play()

def button_A2():
    button_frame(frame_A2)
    pygame.mixer.init()
    pygame.mixer.music.stop()
    pygame.mixer.music.load('D:/งาน/project/GUIS/speak/button2.mp3')
    pygame.mixer.music.play()

def button_A3():
    button_frame(frame_A3)
    pygame.mixer.init()
    pygame.mixer.music.stop()
    pygame.mixer.music.load('D:/งาน/project/GUIS/speak/button3.mp3')
    pygame.mixer.music.play()


# สร้าง GUI
root = tk.Tk()
userInput = tk.StringVar()
root.state('zoomed')

notebook = ttk.Notebook(root)

# Home
frame_home = ttk.Frame(notebook)

image_path = 'D:/งาน/project/GUIS/Image/Canva/Bg.png'
image = Image.open(image_path)
image = image.resize((1920, 1080))
background_photo = ImageTk.PhotoImage(image)
label_background_home = tk.Label(frame_home, image=background_photo)
label_background_home.image = background_photo  # อย่าลืมเก็บอ้างอิงภาพเพื่อป้องกันการแสดงผลผิดพลาด
label_background_home.place(x=0, y=0)
# อาคาร
frame_A1 = ttk.Frame(notebook)

button_A1a = tk.Button(frame_A1, text="อาคารเรียนแผนกวิชาสามัญสัมพันธ์", command=BM.button_a1a)
button_A1a.place(x=10, y=10, width=300, height=30)

button_A1b = tk.Button(frame_A1, text="อาคารเรียน3", command=BM.button_a1b)
button_A1b.place(x=10, y=50, width=300, height=30)

button_A1c = tk.Button(frame_A1, text="อาคารปฎิบัติการช่างไฟฟ้า", command=BM.button_a1c)
button_A1c.place(x=10, y=90, width=300, height=30)

button_A1d = tk.Button(frame_A1, text="อาคารปฎิบัติการช่างก่อสร้าง", command=BM.button_a1d)
button_A1d.place(x=10, y=130, width=300, height=30)

button_A1e = tk.Button(frame_A1, text="อาคารปฎิบัติการช่างกลโรงงาน")
button_A1e.place(x=10, y=170, width=300, height=30)

button_A1f = tk.Button(frame_A1, text="อาคารปฎิบัติการอิเล็กทรอนิกส์")
button_A1f.place(x=10, y=210, width=300, height=30)

button_A1g = tk.Button(frame_A1, text="อาคารปฎิบัติการช่างยนต์")
button_A1g.place(x=10, y=250, width=300, height=30)

button_A1h = tk.Button(frame_A1, text="อาคารปฎิบัติการเทคนิคพื้นฐาน")
button_A1h.place(x=10, y=290, width=300, height=30)

button_A1i = tk.Button(frame_A1, text="อาคารปฎิบัติการ 4 ชั้น")
button_A1i.place(x=10, y=330, width=300, height=30)

# อาคารสำนักงาน
frame_A2 = ttk.Frame(notebook)

button_A2a = tk.Button(frame_A2, text="อสจ.เชียงราย")
button_A2a.place(x=10, y=10, width=300, height=30)

button_A2b = tk.Button(frame_A2, text="อาคารอำนวยการ")
button_A2b.place(x=10, y=50, width=300, height=30)

button_A2c = tk.Button(frame_A2, text="อาคารวิทยบริการ")
button_A2c.place(x=10, y=90, width=300, height=30)

# คำถามที่พบบ่อย
frame_A3 = ttk.Frame(notebook)

button_A3a = tk.Button(frame_A3, text="ctc.ac.th", command=BW.ctcweb)
button_A3a.place(x=10, y=10, width=300, height=30)

# ค้นหา
frame_A4 = ttk.Frame(notebook)
label_A4 = tk.Label(frame_A4, text="ค้นหา")
label_A4.grid(row=0, column=0, columnspan=3, pady=10)

label_A4a = tk.Label(frame_A4, text="คำถาม")
label_A4a.grid(row=0, column=0)

Input_A4a = tk.Entry(frame_A4, textvariable=userInput)
Input_A4a.grid(row=0, column=1)

button_A4a = tk.Button(frame_A4, text="ค้นหา", command=Out_A4a)
button_A4a.place(x=10, y=50, width=100, height=30)

# แท็บ
notebook.add(frame_home, text='Home')
notebook.add(frame_A1, text='อาคารเรียน')
notebook.add(frame_A2, text='อาคารสำนักงาน')
notebook.add(frame_A3, text='คำถามที่พบบ่อย')
notebook.add(frame_A4, text='ค้นหา')

# Frame

text1_image_path = 'D:/งาน/project/GUIS/Image/text/bgtx.png'
text1_image = Image.open(text1_image_path)
text1_image = text1_image.resize((250, 250))
text_photo = ImageTk.PhotoImage(text1_image)
text1 = tk.Label(frame_home, image=text_photo)
text1.image = text_photo
text1.place(x=350, y=250)

text2_image_path = 'D:/งาน/project/GUIS/Image/text/bgtx.png'
text2_image = Image.open(text2_image_path)
text2_image = text2_image.resize((250, 250))
text_photo = ImageTk.PhotoImage(text2_image)
text2 = tk.Label(frame_home, image=text_photo)
text2.image = text_photo
text2.place(x=600, y=620)

text3_image_path = 'D:/งาน/project/GUIS/Image/text/bgt.png'
text3_image = Image.open(text3_image_path)
text3_image = text3_image.resize((250, 250))
text_photo = ImageTk.PhotoImage(text3_image)
text3 = tk.Label(frame_home, image=text_photo)
text3.image = text_photo
text3.place(x=1320, y=250)

text4_image_path = 'D:/งาน/project/GUIS/Image/text/bgt.png'
text4_image = Image.open(text4_image_path)
text4_image = text4_image.resize((250, 250))
text_photo = ImageTk.PhotoImage(text4_image)
text4 = tk.Label(frame_home, image=text_photo)
text4.image = text_photo
text4.place(x=1100, y=620)

button1_image_path = 'D:/งาน/project/GUIS/Image/Canva/GUI2.png'
button1_image = Image.open(button1_image_path)
button1_image = button1_image.resize((100, 100))
button1_photo = ImageTk.PhotoImage(button1_image)
button1 = tk.Button(frame_home, image=button1_photo, text="อาคารเรียน", command=lambda: button_A1())
button1.image = button1_photo
button1.place(x=320, y=190)

button2_image_path = 'D:/งาน/project/GUIS/Image/Canva/GUI2.png'
button2_image = Image.open(button2_image_path)
button2_image = button2_image.resize((100, 100))
button2_photo = ImageTk.PhotoImage(button2_image)
button2 = tk.Button(frame_home, image=button2_photo, text="อาคารสำนักงาน", command=lambda: button_A2())
button2.image = button2_photo
button2.place(x=560, y=570)

button3_image_path = 'D:/งาน/project/GUIS/Image/Canva/GUI2.png'
button3_image = Image.open(button3_image_path)
button3_image = button3_image.resize((100, 100))
button3_photo = ImageTk.PhotoImage(button3_image)
button3 = tk.Button(frame_home, image=button3_photo, text="คำถามที่พบบ่อย", command=lambda: button_A3())
button3.image = button3_photo
button3.place(x=1500, y=190)

button4_image_path = 'D:/งาน/project/GUIS/Image/Canva/GUI2.png'
button4_image = Image.open(button4_image_path)
button4_image = button4_image.resize((100, 100))
button4_photo = ImageTk.PhotoImage(button4_image)
button4 = tk.Button(frame_home, image=button4_photo, text="ค้นหา", command=lambda: button_frame(frame_A4))
button4.image = button4_photo
button4.place(x=1280, y=550)

# ย้อนกลับ
back_button1 = tk.Button(frame_A1, text="กลับสู่หน้า Home", command=lambda: button_frame(frame_home))
back_button1.place(x=10, y=370, width=150, height=30)

back_button2 = tk.Button(frame_A2, text="กลับสู่หน้า Home", command=lambda: button_frame(frame_home))
back_button2.place(x=10, y=370, width=150, height=30)

back_button3 = tk.Button(frame_A3, text="กลับสู่หน้า Home", command=lambda: button_frame(frame_home))
back_button3.place(x=10, y=370, width=150, height=30)

back_button4 = tk.Button(frame_A4, text="กลับสู่หน้า Home", command=lambda: button_frame(frame_home))
back_button4.place(x=10, y=370, width=150, height=30)

notebook.pack(expand=True, fill='both')

root.mainloop()
