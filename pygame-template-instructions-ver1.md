### Pygame: Basic Game Window Template

#### When Finished

- Run your script in VS Code and make sure an empty Pygame window pops up on your computer screen!

#### Steps:

1. **Import Pygame and the `sys` Modules**:
   ```python
   import pygame
   import sys
   ```


2. **Define CONSTANTS**
    ```python
    SCREEN_WIDTH = 800
    SCREEN_HEIGHT = 600

    FPS = 60  # Frames per second

    WHITE = (255, 255, 255) # RGB triplet saved in a tuple
    ```

3. **Initialize Pygame Module**:
   ```python
   pygame.init()
   ```

4. **Set up the window**:
   ```python
   screen = pygame.display.set_mode((SCREEN_WIDTH, SCREEN_HEIGHT))  
   pygame.display.set_caption('Game Title')
   ```

5. **Set up clock**
    ```python
    clock = pygame.time.Clock() # UPPERCASE C at end when typing pygame.time.Clock( )
    ```
6. **Build main game loop**:
   ```python
   running = True
   while running:

       for event in pygame.event.get():     # Listen for and handle events
           if event.type == pygame.QUIT: # Write QUIT event in UPPERCASE!
               running = False
       
       screen.fill(WHITE)  # Fill screen background with white
       pygame.display.update()  # Update the display
   ```

7. **Limit number of frames per second (FPS)**
    ```python
    clock.tick(FPS) # Write this line of code directly under 'pygame.display.update( )' (with same indentation)
    ```

8. **Quit Pygame and `sys` Modules**:
   ```python
   # Write these two lines of code against the left margin and
   # outside the WHILE loop!
   pygame.quit()
   sys.exit()
   ```
---

### Summary:
- **Initialize** Pygame and create a game window.
- In the **main loop**, handle events and refresh the screen with a white background.
- **Exit** cleanly by quitting Pygame and exiting the `sys` module.

