# TkinterOpenCV
#a tkinter,opencv python project

import tkinter as tk
import tkinter.font as font
from PIL import ImageTk,Image
import cv2
import matplotlib.pyplot as plt
root=tk.Tk()
root.title('Avengers')
root.geometry('600x600')


my_img1=ImageTk.PhotoImage(Image.open('tony stark.jpg'))
my_img2=ImageTk.PhotoImage(Image.open('iron snap.jpg'))
my_img3=ImageTk.PhotoImage(Image.open('cap ham.jpg'))
my_img4=ImageTk.PhotoImage(Image.open('cap in.jpg'))
my_img5=ImageTk.PhotoImage(Image.open('thor be.jpg'))
my_img6=ImageTk.PhotoImage(Image.open('thor en.jpg'))
my_img7=ImageTk.PhotoImage(Image.open('hulk en.jpg'))
my_img8=ImageTk.PhotoImage(Image.open('bb.jpg'))
my_img9=ImageTk.PhotoImage(Image.open('bw.jpg'))
my_img10=ImageTk.PhotoImage(Image.open('bw1.jpg'))
my_img11=ImageTk.PhotoImage(Image.open('haw.jpg'))
my_img12=ImageTk.PhotoImage(Image.open('ha1.jpg'))
av_img=ImageTk.PhotoImage(Image.open('av.jpg'))
my_img13=ImageTk.PhotoImage(Image.open('wa.jpg'))
my_img14=ImageTk.PhotoImage(Image.open('wv.jpg'))
my_img15=ImageTk.PhotoImage(Image.open('vi be.jpg'))
my_img16=ImageTk.PhotoImage(Image.open('wava.jpg'))



my_font=font.Font(family='Helvetica')
label_name=tk.Label(root,text='Choose',font=my_font)
label_name.grid(row=0,column=0)

def crop():
    ironman1=cv2.imread('iron man.jpg')
    crop_iron=ironman1[70:150,100:160]
    plt.imshow(cv2.cvtColor(crop_iron,cv2.COLOR_BGR2RGB))
    plt.title('wanna see the face?')
    plt.axis('off')
    plt.show()
def size():
    ironman2=cv2.imread('iron man.jpg')
    print('size: ' ,ironman2.shape)
    
def maxmin():
    ironman=cv2.imread('iron man.jpg')
    print('max pixel is ',ironman.max(),'and min pixel is ',ironman.min())
    
def gray():
    ironman=cv2.imread('iron man.jpg',0)
    plt.imshow(ironman,cmap='gray',interpolation='bicubic')
    plt.title('1960s ironman')
    plt.axis('off')
    plt.show()
    
def bgr():
    ironman=cv2.imread('iron man.jpg')
    plt.imshow(ironman)
    plt.title('BGR ironman')
    plt.axis('off')
    plt.show()
    
def face ():
    ironman=cv2.imread('iron man.jpg')
    ironman[70:150,100:160]=[255,255,255]
    plt.imshow(cv2.cvtColor(ironman,cv2.COLOR_BGR2RGB))
    plt.title('Where is the face?')
    plt.axis('off')
    plt.show()
    
def resize():
    ironman=cv2.imread('iron man.jpg')
    resized=cv2.resize(ironman,(100,100))
    plt.imshow(cv2.cvtColor(resized,cv2.COLOR_BGR2RGB))
    plt.title('ironman disturbed')
    plt.axis('off')
    plt.show()
    
    
    
    
    
    
    
    

def rdj():
    ironman=cv2.imread('iron man.jpg')
    plt.imshow(cv2.cvtColor(ironman,cv2.COLOR_BGR2RGB))
    plt.title('iron man')
    plt.axis('off')
    plt.show()
    #root.destroy()
    rdjwindow=tk.Toplevel()
    rdjwindow.title('IRON MAN-TONY STARK')
    rdjwindow.geometry('600x600')
    btn1 = tk.Button(rdjwindow,text='wanna crop?', height=10, width=20, font=my_font, background='red',command=crop)
    btn1.grid(row=0, column=0)
    btn2 = tk.Button(rdjwindow,text='wanna know the size?', height=10, width=20, font=my_font, background='red',command=size)
    btn2.grid(row=0, column=1)
    btn3 = tk.Button(rdjwindow,text='max and min pixel?', height=10, width=20, font=my_font, background='red',command=maxmin)
    btn3.grid(row=0, column=2)
    btn4 = tk.Button(rdjwindow,text='gray scale?', height=10, width=20, font=my_font, background='red',command=gray)
    btn4.grid(row=1, column=0)
    btn5 = tk.Button(rdjwindow,text='BGR?', height=10, width=20, font=my_font, background='red',command=bgr)
    btn5.grid(row=1, column=1)
    btn6 = tk.Button(rdjwindow,text='hide the face?', height=10, width=20, font=my_font, background='red',command=face)
    btn6.grid(row=1, column=2)
    btn7 = tk.Button(rdjwindow,text='resize?', height=10, width=20, font=my_font, background='red',command=resize)
    btn7.grid(row=2, column=0)
    label_tony_pic = tk.Label(rdjwindow, image=my_img1,height=200, width=200)
    label_tony_pic.grid(row=2, column=1)
    label_tony_pic1 = tk.Label(rdjwindow, image=my_img2,height=200, width=200)
    label_tony_pic1.grid(row=2, column=2)
    
    
    
    
    
    
    
button_iron=tk.Button(root,text='iron man',height=10,width=20,font=my_font,background='red',command=rdj)
button_iron.grid(row=1,column=0)

def ccrop():
    cap=cv2.imread('cap.jpg')
    crop_cap=cap[0:60,120:170]
    plt.imshow(cv2.cvtColor(crop_cap,cv2.COLOR_BGR2RGB))
    plt.title('wanna see the face?')
    plt.axis('off')
    plt.show()
    
def csize():
    cap=cv2.imread('cap.jpg')
    print('size: ' ,cap.shape)
    
def cmaxmin():
    cap=cv2.imread('cap.jpg')
    print('max pixel is ',cap.max(),'and min pixel is ',cap.min())
    
def cgray():
    cap=cv2.imread('cap.jpg',0)
    plt.imshow(cap,cmap='gray',interpolation='bicubic')
    plt.title('Before napping in ice')
    plt.axis('off')
    plt.show()
    
def cbgr():
    cap=cv2.imread('cap.jpg')
    plt.imshow(cap)
    plt.title('BGR cap')
    plt.axis('off')
    plt.show()
    
def cface():
    cap=cv2.imread('cap.jpg')
    cap[0:60,120:170]=[255,255,255]
    plt.imshow(cv2.cvtColor(cap,cv2.COLOR_BGR2RGB))
    plt.title('Where is the face?')
    plt.axis('off')
    plt.show()
    
def cresize():
    cap=cv2.imread('cap.jpg')
    resized=cv2.resize(cap,(100,100))
    plt.imshow(cv2.cvtColor(resized,cv2.COLOR_BGR2RGB))
    plt.title('cap disturbed')
    plt.axis('off')
    plt.show()
    
    
    

    
    
    
    


def ce():
    cap=cv2.imread('cap.jpg')
    plt.imshow(cv2.cvtColor(cap,cv2.COLOR_BGR2RGB))
    plt.title('Captain America')
    plt.axis('off')
    plt.show()
    rdjwindow=tk.Toplevel()
    rdjwindow.title('CAPTAIN AMERICA-STEVE ROGERS')
    rdjwindow.geometry('600x600')
    btn1 = tk.Button(rdjwindow,text='wanna crop?', height=10, width=20, font=my_font, background='white',command=ccrop)
    btn1.grid(row=0, column=0)
    btn2 = tk.Button(rdjwindow,text='wanna know the size?', height=10, width=20, font=my_font, background='white',command=csize)
    btn2.grid(row=0, column=1)
    btn3 = tk.Button(rdjwindow,text='max and min pixel?', height=10, width=20, font=my_font, background='white',command=cmaxmin)
    btn3.grid(row=0, column=2)
    btn4 = tk.Button(rdjwindow,text='gray scale?', height=10, width=20, font=my_font, background='white',command=cgray)
    btn4.grid(row=1, column=0)
    btn5 = tk.Button(rdjwindow,text='BGR?', height=10, width=20, font=my_font, background='white',command=cbgr)
    btn5.grid(row=1, column=1)
    btn6 = tk.Button(rdjwindow,text='hide the face?', height=10, width=20, font=my_font, background='white',command=cface)
    btn6.grid(row=1, column=2)
    btn7 = tk.Button(rdjwindow,text='resize?', height=10, width=20, font=my_font, background='white',command=cresize)
    btn7.grid(row=2, column=0)
    label_cap_pic = tk.Label(rdjwindow, image=my_img3,height=200, width=200)
    label_cap_pic.grid(row=2, column=1)
    label_cap_pic1 = tk.Label(rdjwindow, image=my_img4,height=200, width=200)
    label_cap_pic1.grid(row=2, column=2)
    

button_cap=tk.Button(root,text="Captain America",height=10,width=20,font=my_font,background='white',command=ce)
button_cap.grid(row=1,column=1)


def tcrop():
    cap=cv2.imread('thor.jpg')
    crop_cap=cap[0:40,150:200]
    plt.imshow(cv2.cvtColor(crop_cap,cv2.COLOR_BGR2RGB))
    plt.title('wanna see the face?')
    plt.axis('off')
    plt.show()

def tsize():
    cap=cv2.imread('thor.jpg')
    print('size: ' ,cap.shape)
    
def tmaxmin():
    cap=cv2.imread('thor.jpg')
    print('max pixel is ',cap.max(),'and min pixel is ',cap.min())
    
def tgray():
    cap=cv2.imread('thor.jpg',0)
    plt.imshow(cap,cmap='gray',interpolation='bicubic')
    plt.title('During his 2000th birthday')
    plt.axis('off')
    plt.show()
    
def tbgr():
    cap=cv2.imread('thor.jpg')
    plt.imshow(cap)
    plt.title('BGR thor')
    plt.axis('off')
    plt.show()
    
def tface():
    cap=cv2.imread('thor.jpg')
    cap[0:40,150:200]=[255,255,255]
    plt.imshow(cv2.cvtColor(cap,cv2.COLOR_BGR2RGB))
    plt.title('Where is the face?')
    plt.axis('off')
    plt.show()

def tresize():
    cap=cv2.imread('thor.jpg')
    resized=cv2.resize(cap,(100,100))
    plt.imshow(cv2.cvtColor(resized,cv2.COLOR_BGR2RGB))
    plt.title('thor disturbed')
    plt.axis('off')
    plt.show()
    
    
    
    
    
    
    
    

def ch():
    thor=cv2.imread('thor.jpg')
    plt.imshow(cv2.cvtColor(thor,cv2.COLOR_BGR2RGB))
    plt.title('Thor')
    plt.axis('off')
    plt.show()
    rdjwindow=tk.Toplevel()
    rdjwindow.title('THOR-THOR')
    rdjwindow.geometry('600x600')
    btn1 = tk.Button(rdjwindow,text='wanna crop?', height=10, width=20, font=my_font, background='blue',command=tcrop)
    btn1.grid(row=0, column=0)
    btn2 = tk.Button(rdjwindow,text='wanna know the size?', height=10, width=20, font=my_font, background='blue',command=tsize)
    btn2.grid(row=0, column=1)
    btn3 = tk.Button(rdjwindow,text='max and min pixel?', height=10, width=20, font=my_font, background='blue',command=tmaxmin)
    btn3.grid(row=0, column=2)
    btn4 = tk.Button(rdjwindow,text='gray scale?', height=10, width=20, font=my_font, background='blue',command=tgray)
    btn4.grid(row=1, column=0)
    btn5 = tk.Button(rdjwindow,text='BGR?', height=10, width=20, font=my_font, background='blue',command=tbgr)
    btn5.grid(row=1, column=1)
    btn6 = tk.Button(rdjwindow,text='hide the face?', height=10, width=20, font=my_font, background='blue',command=tface)
    btn6.grid(row=1, column=2)
    btn7 = tk.Button(rdjwindow,text='resize?', height=10, width=20, font=my_font, background='blue',command=tresize)
    btn7.grid(row=2, column=0)
    label_cap_pic = tk.Label(rdjwindow, image=my_img5,height=200, width=200)
    label_cap_pic.grid(row=2, column=1)
    label_cap_pic1 = tk.Label(rdjwindow, image=my_img6,height=200, width=200)
    label_cap_pic1.grid(row=2, column=2)       
    
button_thor=tk.Button(root,text="Thor",height=10,width=20,font=my_font,background='blue',command=ch)
button_thor.grid(row=1,column=2)


def hcrop():
    cap=cv2.imread('hulk.jpg')
    crop_cap=cap[0:100,70:200]
    plt.imshow(cv2.cvtColor(crop_cap,cv2.COLOR_BGR2RGB))
    plt.title('wanna see the face?')
    plt.axis('off')
    plt.show()
    
def hsize():
    cap=cv2.imread('hulk.jpg')
    print('size: ' ,cap.shape)
def hmaxmin():
    cap=cv2.imread('hulk.jpg')
    print('max pixel is ',cap.max(),'and min pixel is ',cap.min())
    
def hgray():
    cap=cv2.imread('hulk.jpg',0)
    plt.imshow(cap,cmap='gray',interpolation='bicubic')
    plt.title('Grey hulk')
    plt.axis('off')
    plt.show()
    
def hbgr():
    cap=cv2.imread('hulk.jpg')
    plt.imshow(cap)
    plt.title('BGR hulk')
    plt.axis('off')
    plt.show()
    
def hface(): 
    cap=cv2.imread('hulk.jpg')
    cap[0:100,70:200]=[255,255,255]
    plt.imshow(cv2.cvtColor(cap,cv2.COLOR_BGR2RGB))
    plt.title('Where is the face?')
    plt.axis('off')
    plt.show()
    
def hresize():
    cap=cv2.imread('hulk.jpg')
    resized=cv2.resize(cap,(100,100))
    plt.imshow(cv2.cvtColor(resized,cv2.COLOR_BGR2RGB))
    plt.title('a very disturbed hulk')
    plt.axis('off')
    plt.show()
    
    
    
    
    
    
    
    
    
    
    
def bb():
    hulk=cv2.imread('hulk.jpg')
    plt.imshow(cv2.cvtColor(hulk,cv2.COLOR_BGR2RGB))
    plt.title('Hulk')
    plt.axis('off')
    plt.show()
    rdjwindow=tk.Toplevel()
    rdjwindow.title('HULK-BRUCE BANNER')
    rdjwindow.geometry('600x600')
    btn1 = tk.Button(rdjwindow,text='wanna crop?', height=10, width=20, font=my_font, background='green',command=hcrop)
    btn1.grid(row=0, column=0)
    btn2 = tk.Button(rdjwindow,text='wanna know the size?', height=10, width=20, font=my_font, background='green',command=hsize)
    btn2.grid(row=0, column=1)
    btn3 = tk.Button(rdjwindow,text='max and min pixel?', height=10, width=20, font=my_font, background='green',command=hmaxmin)
    btn3.grid(row=0, column=2)
    btn4 = tk.Button(rdjwindow,text='gray scale?', height=10, width=20, font=my_font, background='green',command=hgray)
    btn4.grid(row=1, column=0)
    btn5 = tk.Button(rdjwindow,text='BGR?', height=10, width=20, font=my_font, background='green',command=hbgr)
    btn5.grid(row=1, column=1)
    btn6 = tk.Button(rdjwindow,text='hide the face?', height=10, width=20, font=my_font, background='green',command=hface)
    btn6.grid(row=1, column=2)
    btn7 = tk.Button(rdjwindow,text='resize?', height=10, width=20, font=my_font, background='green',command=hresize)
    btn7.grid(row=2, column=0)
    label_cap_pic = tk.Label(rdjwindow, image=my_img7,height=200, width=200)
    label_cap_pic.grid(row=2, column=1)
    label_cap_pic1 = tk.Label(rdjwindow, image=my_img8,height=200, width=200)
    label_cap_pic1.grid(row=2, column=2)

button_hulk=tk.Button(root,text='hulk',height=10,width=20,font=my_font,background='green',command=bb)
button_hulk.grid(row=2,column=0)


def bcrop():
    cap=cv2.imread('blackwidow.jpg')
    crop_cap=cap[40:110,50:120]
    plt.imshow(cv2.cvtColor(crop_cap,cv2.COLOR_BGR2RGB))
    plt.title('wanna see the face?')
    plt.axis('off')
    plt.show()
    
def bsize():
    cap=cv2.imread('blackwidow.jpg')
    print('size: ' ,cap.shape)
def bmaxmin():
    cap=cv2.imread('blackwidow.jpg')  
    print('max pixel is ',cap.max(),'and min pixel is ',cap.min())
def bgray():
    cap=cv2.imread('blackwidow.jpg',0)
    plt.imshow(cap,cmap='gray',interpolation='bicubic')
    plt.title('blacky widow')
    plt.axis('off')
    plt.show()
def bbgr():
    cap=cv2.imread('blackwidow.jpg')
    plt.imshow(cap)
    plt.title('BGR blackwidow')
    plt.axis('off')
    plt.show()
def bface():
    cap=cv2.imread('blackwidow.jpg')
    cap[40:110,50:120]=[255,255,255]
    plt.imshow(cv2.cvtColor(cap,cv2.COLOR_BGR2RGB))
    plt.title('Where is the face?')
    plt.axis('off')
    plt.show()
def bresize():
    cap=cv2.imread('blackwidow.jpg')
    resized=cv2.resize(cap,(100,100))
    plt.imshow(cv2.cvtColor(resized,cv2.COLOR_BGR2RGB))
    plt.title('disturbed blackwidow')
    plt.axis('off')
    plt.show()
    
    
    

    
    
    

def sj():
    hulk=cv2.imread('blackwidow.jpg')
    plt.imshow(cv2.cvtColor(hulk,cv2.COLOR_BGR2RGB))
    plt.title('Black Widow')
    plt.axis('off')
    plt.show()
    rdjwindow=tk.Toplevel()
    rdjwindow.title('BLACK WIDOW-NATASHA ROMANAFF')
    rdjwindow.geometry('600x600')
    btn1 = tk.Button(rdjwindow,text='wanna crop?', height=10, width=20, font=my_font, background='gray',command=bcrop)
    btn1.grid(row=0, column=0)
    btn2 = tk.Button(rdjwindow,text='wanna know the size?', height=10, width=20, font=my_font, background='gray',command=bsize)
    btn2.grid(row=0, column=1)
    btn3 = tk.Button(rdjwindow,text='max and min pixel?', height=10, width=20, font=my_font, background='gray',command=bmaxmin)
    btn3.grid(row=0, column=2)
    btn4 = tk.Button(rdjwindow,text='gray scale?', height=10, width=20, font=my_font, background='gray',command=bgray)
    btn4.grid(row=1, column=0)
    btn5 = tk.Button(rdjwindow,text='BGR?', height=10, width=20, font=my_font, background='gray',command=bbgr)
    btn5.grid(row=1, column=1)
    btn6 = tk.Button(rdjwindow,text='hide the face?', height=10, width=20, font=my_font, background='gray',command=bface)
    btn6.grid(row=1, column=2)
    btn7 = tk.Button(rdjwindow,text='resize?', height=10, width=20, font=my_font, background='gray',command=bresize)
    btn7.grid(row=2, column=0)
    label_cap_pic = tk.Label(rdjwindow, image=my_img9,height=200, width=200)
    label_cap_pic.grid(row=2, column=1)
    label_cap_pic1 = tk.Label(rdjwindow, image=my_img10,height=200, width=200)
    label_cap_pic1.grid(row=2, column=2)
    
button_widow=tk.Button(root,text="Black Widow",height=10,width=20,font=my_font,background='gray',command=sj)
button_widow.grid(row=2,column=1)
def jcrop():
    cap=cv2.imread('hawkeye.jpg')
    crop_cap=cap[5:50,40:100]
    plt.imshow(cv2.cvtColor(crop_cap,cv2.COLOR_BGR2RGB))
    plt.title('wanna see the face?')
    plt.axis('off')
    plt.show()
def jsize():
    cap=cv2.imread('hawkeye.jpg')
    print('size: ' ,cap.shape)
    
def jmaxmin():
    cap=cv2.imread('hawkeye.jpg')    
    print('max pixel is ',cap.max(),'and min pixel is ',cap.min())
def jgray():
    cap=cv2.imread('hawkeye.jpg',0)
    plt.imshow(cap,cmap='gray',interpolation='bicubic')
    plt.title('Black Bird')
    plt.axis('off')
    plt.show()
def jbgr():
    cap=cv2.imread('hawkeye.jpg') 
    plt.imshow(cap)
    plt.title('BGR hawkeye')
    plt.axis('off')
    plt.show()
def jface():
    cap=cv2.imread('hawkeye.jpg')
    cap[5:50,40:100]=[255,255,255]
    plt.imshow(cv2.cvtColor(cap,cv2.COLOR_BGR2RGB))
    plt.title('Where is the face?')
    plt.axis('off')
    plt.show()
def jresize():
    cap=cv2.imread('hawkeye.jpg')
    resized=cv2.resize(cap,(100,100))
    plt.imshow(cv2.cvtColor(resized,cv2.COLOR_BGR2RGB))
    plt.title('hawkeye disturbed ')
    plt.axis('off')
    plt.show()
    



    
    
    
    
    
    
def jr():
    hulk=cv2.imread('hawkeye.jpg')
    plt.imshow(cv2.cvtColor(hulk,cv2.COLOR_BGR2RGB))
    plt.title('Hawkeye')
    plt.axis('off')
    plt.show()
    rdjwindow=tk.Toplevel()
    rdjwindow.title('HAWKEYE-CINTON BARTON')
    rdjwindow.geometry('600x600')
    btn1 = tk.Button(rdjwindow,text='wanna crop?', height=10, width=20, font=my_font, background='dark gray',command=jcrop)
    btn1.grid(row=0, column=0)
    btn2 = tk.Button(rdjwindow,text='wanna know the size?', height=10, width=20, font=my_font, background='dark gray',command=jsize)
    btn2.grid(row=0, column=1)
    btn3 = tk.Button(rdjwindow,text='max and min pixel?', height=10, width=20, font=my_font, background='dark gray',command=jmaxmin)
    btn3.grid(row=0, column=2)
    btn4 = tk.Button(rdjwindow,text='gray scale?', height=10, width=20, font=my_font, background='dark gray',command=jgray)
    btn4.grid(row=1, column=0)
    btn5 = tk.Button(rdjwindow,text='BGR?', height=10, width=20, font=my_font, background='dark gray',command=jbgr)
    btn5.grid(row=1, column=1)
    btn6 = tk.Button(rdjwindow,text='hide the face?', height=10, width=20, font=my_font, background='dark gray',command=jface)
    btn6.grid(row=1, column=2)
    btn7 = tk.Button(rdjwindow,text='resize?', height=10, width=20, font=my_font, background='dark gray',command=jresize)
    btn7.grid(row=2, column=0)
    label_cap_pic = tk.Label(rdjwindow, image=my_img11,height=200, width=200)
    label_cap_pic.grid(row=2, column=1)
    label_cap_pic1 = tk.Label(rdjwindow, image=my_img12,height=200, width=200)
    label_cap_pic1.grid(row=2, column=2)
    
button_hawk=tk.Button(root,text="Hawkeye",height=10,width=20,font=my_font,background='dark gray',command=jr)
button_hawk.grid(row=2,column=2)
def wcrop():
    cap=cv2.imread('sw.jpg')
    crop_cap=cap[0:100,70:170]
    plt.imshow(cv2.cvtColor(crop_cap,cv2.COLOR_BGR2RGB))
    plt.title('wanna see the face?')
    plt.axis('off')
    plt.show()
    
def wsize():
    cap=cv2.imread('sw.jpg')
    print('size: ' ,cap.shape)
def wmaxmin():
    cap=cv2.imread('sw.jpg')
    print('max pixel is ',cap.max(),'and min pixel is ',cap.min())
def wgray():
    cap=cv2.imread('sw.jpg',0)
    plt.imshow(cap,cmap='gray',interpolation='bicubic')
    plt.title('in her 1950s sitcom')
    plt.axis('off')
    plt.show()
def wbgr():
    cap=cv2.imread('sw.jpg')
    plt.imshow(cap)
    plt.title('BGR Wanda')
    plt.axis('off')
    plt.show()
def wface():
    cap=cv2.imread('sw.jpg')
    cap[0:100,70:170]=[255,255,255]
    plt.imshow(cv2.cvtColor(cap,cv2.COLOR_BGR2RGB))
    plt.title('Where is the face?')
    plt.axis('off')
    plt.show()
def wresize():
    cap=cv2.imread('sw.jpg')
    resized=cv2.resize(cap,(100,100))
    plt.imshow(cv2.cvtColor(resized,cv2.COLOR_BGR2RGB))
    plt.title('a very disturbed wanda')
    plt.axis('off')
    plt.show()
    
    
    

    
    
def eo():
    hulk=cv2.imread('sw.jpg')
    plt.imshow(cv2.cvtColor(hulk,cv2.COLOR_BGR2RGB))
    plt.title('Scarlet Witch')
    plt.axis('off')
    plt.show()
    rdjwindow=tk.Toplevel()
    rdjwindow.title('SCARLET WITCH-WANDA MAXIMOFF')
    rdjwindow.geometry('600x600')
    btn1 = tk.Button(rdjwindow,text='wanna crop?', height=10, width=20, font=my_font, background='orangered',command=wcrop)
    btn1.grid(row=0, column=0)
    btn2 = tk.Button(rdjwindow,text='wanna know the size?', height=10, width=20, font=my_font, background='orangered',command=wsize)
    btn2.grid(row=0, column=1)
    btn3 = tk.Button(rdjwindow,text='max and min pixel?', height=10, width=20, font=my_font, background='orangered',command=wmaxmin)
    btn3.grid(row=0, column=2)
    btn4 = tk.Button(rdjwindow,text='gray scale?', height=10, width=20, font=my_font, background='orangered',command=wgray)
    btn4.grid(row=1, column=0)
    btn5 = tk.Button(rdjwindow,text='BGR?', height=10, width=20, font=my_font, background='orangered',command=wbgr)
    btn5.grid(row=1, column=1)
    btn6 = tk.Button(rdjwindow,text='hide the face?', height=10, width=20, font=my_font, background='orangered',command=wface)
    btn6.grid(row=1, column=2)
    btn7 = tk.Button(rdjwindow,text='resize?', height=10, width=20, font=my_font, background='orangered',command=wresize)
    btn7.grid(row=2, column=0)
    label_cap_pic = tk.Label(rdjwindow, image=my_img13,height=200, width=200)
    label_cap_pic.grid(row=2, column=1)
    label_cap_pic1 = tk.Label(rdjwindow, image=my_img14,height=200, width=200)
    label_cap_pic1.grid(row=2, column=2)
    

button_wanda=tk.Button(root,text="Scarlet Witch",height=10,width=20,font=my_font,background='orangered',command=eo)
button_wanda.grid(row=3,column=0)
def pcrop():
    cap=cv2.imread('vis.jpg')
    crop_cap=cap[40:80,70:120]
    plt.imshow(cv2.cvtColor(crop_cap,cv2.COLOR_BGR2RGB))
    plt.title('wanna see the face?')
    plt.axis('off')
    plt.show()
def psize():
    cap=cv2.imread('vis.jpg')
    print('size: ' ,cap.shape)
def pmaxmin():
    cap=cv2.imread('vis.jpg')
    print('max pixel is ',cap.max(),'and min pixel is ',cap.min())
def pgray():
    cap=cv2.imread('vis.jpg',0)
    plt.imshow(cap,cmap='gray',interpolation='bicubic')
    plt.title('After the stone is plucked')
    plt.axis('off')
    plt.show()
def pbgr():
    cap=cv2.imread('vis.jpg')
    plt.imshow(cap)
    plt.title('BGR vision')
    plt.axis('off')
    plt.show()
def pface():
    cap=cv2.imread('vis.jpg')
    cap[40:80,70:120]=[255,255,255]
    plt.imshow(cv2.cvtColor(cap,cv2.COLOR_BGR2RGB))
    plt.title('Where is the face?')
    plt.axis('off')
    plt.show()
def presize():
    cap=cv2.imread('vis.jpg')
    resized=cv2.resize(cap,(100,100))
    plt.imshow(cv2.cvtColor(resized,cv2.COLOR_BGR2RGB))
    plt.title('a very disturbed vision')
    plt.axis('off')
    plt.show()    
    
def pb():
    hulk=cv2.imread('vis.jpg')
    plt.imshow(cv2.cvtColor(hulk,cv2.COLOR_BGR2RGB))
    plt.title('Vision')
    plt.axis('off')
    plt.show()
    rdjwindow=tk.Toplevel()
    rdjwindow.title('VISION-VISION')
    rdjwindow.geometry('600x600')
    btn1 = tk.Button(rdjwindow,text='wanna crop?', height=10, width=20, font=my_font, background='firebrick',command=pcrop)
    btn1.grid(row=0, column=0)
    btn2 = tk.Button(rdjwindow,text='wanna know the size?', height=10, width=20, font=my_font, background='firebrick',command=psize)
    btn2.grid(row=0, column=1)
    btn3 = tk.Button(rdjwindow,text='max and min pixel?', height=10, width=20, font=my_font, background='firebrick',command=pmaxmin)
    btn3.grid(row=0, column=2)
    btn4 = tk.Button(rdjwindow,text='gray scale?', height=10, width=20, font=my_font, background='firebrick',command=pgray)
    btn4.grid(row=1, column=0)
    btn5 = tk.Button(rdjwindow,text='BGR?', height=10, width=20, font=my_font, background='firebrick',command=pbgr)
    btn5.grid(row=1, column=1)
    btn6 = tk.Button(rdjwindow,text='hide the face?', height=10, width=20, font=my_font, background='firebrick',command=pface)
    btn6.grid(row=1, column=2)
    btn7 = tk.Button(rdjwindow,text='resize?', height=10, width=20, font=my_font, background='firebrick',command=presize)
    btn7.grid(row=2, column=0)
    label_cap_pic = tk.Label(rdjwindow, image=my_img15,height=200, width=200)
    label_cap_pic.grid(row=2, column=1)
    label_cap_pic1 = tk.Label(rdjwindow, image=my_img16,height=200, width=200)
    label_cap_pic1.grid(row=2, column=2)
    

button_vision=tk.Button(root,text="Vision",height=10,width=20,font=my_font,background='firebrick',command=pb)
button_vision.grid(row=3,column=1)

avengers=tk.Label(root,image=av_img,height=200,width=200)
avengers.grid(row=3,column=2)






root.mainloop()
