# daire
import turtle

def polygon(t, uzunluk, ks):        #Ks : Kenar sayısı
    da = 360 / ks            #Dönüş açısı belirlenir
    for i in range(ks):
        t.forward(uzunluk)       #Belirtilen uzunlukta ileri gider
        t.left(da)               #belirtilen açıda dönüş yapar


def circle(t, r):
    cevre = 2 * 3.14 * r          #Çevre formulü
    ks = int(cevre / 3)           #Yaklaşık kenar sayısını bulmak için çevre üç e bölünür
    uzunluk = cevre / ks
    polygon(t, uzunluk, ks)

wn = turtle.Screen()
wn.bgcolor("Black")

ar = turtle.Turtle()
ar.color("Red")         #Kalem rengi
ar.pensize(2)           #Kalem kalınlığı

circle(ar, 100)

turtle.done()
