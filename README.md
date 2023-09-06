#include <stdio.h>

int min_steps_to_reach(int x, int y) {
    int steps = 0;

    while (x != y) {
        if (x < y) {
            y--;
        }
        else if (x > y) {
            x--;
        }
        steps++;
    }

    return steps;
}

int main() {
    int x = 35, y = 40;
    int steps = min_steps_to_reach(x, y);
    printf("Мінімальна кількість кроків для переходу від %d до %d: %d\n", x, y, steps);
    return 0;
}
