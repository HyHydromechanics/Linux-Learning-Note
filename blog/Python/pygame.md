# **Pygame常用语法**

> [!TIP]
> 窗口设置

```python
size = width, height = 1080,720
bg = (0,0,0) # 也可输入图片路径

#设置背景与标题
screen = pygame.display.set_mode(size) 
pygame. display.set_caption("") #窗口标题
```

> [!TIP]
> 键位设置

```python
while True: #关闭系统
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            sys.exit()
```

```python
if event.type == KEYDOWN:
            if event.key == K_a:
                speed_1 = [-5,0]
                pat_1 = pygame.transform(pat_1, True, True)
```

> [!TIP]
> Pygame的设置为屏幕刷新率而更新本体窗口, 因此每次注入新元素都需要通过屏幕刷新而进行来写入屏幕

```python
screen.blit(x,y) #内置参数
pygame.display.flip()
clock.tick(200) #此处为帧率
```

<p align="center">
<img src="./assets/pic/pygame_setmode.jpg" width="1000" height="574" /></a>
</p>


<p align="center">
<img src="./assets/pic/pygame_typein.jpg" width="1000" height="749" /></a>
</p>


>[!TIP]更多可以直接参考官方文档: https://www.pygame.org/docs/