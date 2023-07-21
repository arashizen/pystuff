# Simple grid that allows the user to color each cell using the mouse button or scroll wheel.
# 10 colors that correspond to each number key, press the keys to see the names of each color. 0 Acts as an eraser, coloring the cell back to its original color.

import pygame
import sys

# Define colors
COLORS = {
    1: (0, 0, 0),
    2: (255, 255, 255),
    3: (255, 0, 0),
    4: (0, 255, 0),
    5: (0, 0, 255),
    6: (255, 165, 0),
    7: (255, 255, 0),
    8: (0, 255, 255),
    9: (255, 0, 255),
    0: (192, 192, 192)
}

COLOR_NAMES = {
    1: 'Black',
    2: 'White',
    3: 'Red',
    4: 'Green',
    5: 'Blue',
    6: 'Orange',
    7: 'Yellow',
    8: 'Cyan',
    9: 'Magenta',
    0: 'Eraser'
}


# Game Settings
GRID_SIZE = 50
CELL_SIZE = 20
WINDOW_WIDTH = GRID_SIZE * CELL_SIZE
WINDOW_HEIGHT = GRID_SIZE * CELL_SIZE
FPS = 60

# Initialize Pygame
pygame.init()
pygame.font.init()
screen = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT))
clock = pygame.time.Clock()


# Initialize grid
grid = [[COLORS[0] for _ in range(GRID_SIZE)] for _ in range(GRID_SIZE)]
color = COLORS[1]
color_name = COLOR_NAMES[1]

while True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()
        if event.type == pygame.KEYDOWN:
            if event.key == pygame.K_1:
                color = COLORS[1]
                color_name = COLOR_NAMES[1]
            elif event.key == pygame.K_2:
                color = COLORS[2]
                color_name = COLOR_NAMES[2]
            elif event.key == pygame.K_3:
                color = COLORS[3]
                color_name = COLOR_NAMES[3]
            elif event.key == pygame.K_4:
                color = COLORS[4]
                color_name = COLOR_NAMES[4]
            elif event.key == pygame.K_5:
                color = COLORS[5]
                color_name = COLOR_NAMES[5]
            elif event.key == pygame.K_6:
                color = COLORS[6]
                color_name = COLOR_NAMES[6]
            elif event.key == pygame.K_7:
                color = COLORS[7]
                color_name = COLOR_NAMES[7]
            elif event.key == pygame.K_8:
                color = COLORS[8]
                color_name = COLOR_NAMES[8]
            elif event.key == pygame.K_9:
                color = COLORS[9]
                color_name = COLOR_NAMES[9]
            elif event.key == pygame.K_0:
                color = COLORS[0]
                color_name = COLOR_NAMES[0]
        if event.type == pygame.MOUSEBUTTONDOWN:
            x, y = pygame.mouse.get_pos()
            grid[y // CELL_SIZE][x // CELL_SIZE] = color

    screen.fill((192, 192, 192))
    for i, row in enumerate(grid):
        for j, col in enumerate(row):
            pygame.draw.rect(screen, col, pygame.Rect(j * CELL_SIZE, i * CELL_SIZE, CELL_SIZE, CELL_SIZE))
            pygame.draw.rect(screen, (0, 0, 0), pygame.Rect(j * CELL_SIZE, i * CELL_SIZE, CELL_SIZE, CELL_SIZE), 1)

    # Render the color name
    font = pygame.font.Font(None, 36)
    text = font.render(color_name, True, (0, 0, 0))
    screen.blit(text, (10, 10))

    pygame.display.update()
    clock.tick(FPS)
r
