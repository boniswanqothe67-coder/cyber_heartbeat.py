# cyber_heartbeat.py
Python terminal animation of a pulsing hacker-style heart with colors and dynamic effects. Designed for fun, aesthetic, and coding showcase.
# ==========================
# ASCII Heart in Python
# ==========================
import time
import sys

RED = "\033[91m"
RESET = "\033[0m"

heart = [
    "  **     **  ",
    " ****   **** ",
    "****** ******",
    " *********** ",
    "  *********  ",
    "   *******   ",
    "    *****    ",
    "     ***     ",
    "      *      "
]

def slow_print(text, delay=0.05):
    for char in text:
        sys.stdout.write(char)
        sys.stdout.flush()
        time.sleep(delay)
    print()

# Print banner
print(f"{RED}❤❤❤ ASCII Heart Generator ❤❤❤{RESET}\n")
time.sleep(0.5)

# Draw the heart
for line in heart:
    slow_print(f"{RED}{line}{RESET}")
    time.sleep(0.1)

print(f"\n{RED}Heart completed! ❤{RESET}")
