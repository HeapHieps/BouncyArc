import pygame
import random
from pygame import mixer

pygame.init()

screen = pygame.display.set_mode((800,600))
pygame.display.set_caption("Bouncy Neco Arc😳")
logo = pygame.image.load('necocomper.gif')
pygame.display.set_icon(logo)

mixer.music.load('Neco Arc meow.mp3')
mixer.music.play(-1)

NecoArc_img = pygame.image.load('long_neco_arc.png')
LongNeco_img = pygame.transform.scale(NecoArc_img,(75,150))
NecoX = random.randint(100,580)
NecoY = random.randint(50,480)
NecoX_MovementX = .2
NecoY_MovementY = -.2

Second_img = pygame.image.load('Fish_Lips.png')
PufferFish = pygame.transform.scale(Second_img,(100,100))
secondImgX = 4000
secondImgY = 250
secondImgX_MovementX = -.9
secondImgY_MovementY = 0

def Neco(x,y):
    screen.blit(LongNeco_img,(x,y))

def SecondImg(x,y):
    screen.blit(PufferFish,(x,y))

running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    Color_first = random.randint(0,255)
    Color_second = random.randint(0,255)
    Color_third = random.randint(0,255)
    Color = Color_first,Color_second,Color_third
    screen.fill((Color))
    
    NecoX += NecoX_MovementX
    NecoY += NecoY_MovementY
    if NecoX <= 0:
        NecoX_MovementX = .2
    if NecoX >= 740:
        NecoX_MovementX = -.2
    if NecoY <= 0:
        NecoY_MovementY = .2
    if NecoY >= 455:
        NecoY_MovementY = -.2

    secondImgX += secondImgX_MovementX
    secondImgY += secondImgY_MovementY
    Neco(NecoX,NecoY)
    SecondImg(secondImgX,secondImgY)
    
    pygame.display.update()
