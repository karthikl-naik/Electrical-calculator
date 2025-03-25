# Electrical-calculator
//calculator for electrical quantities
#include <stdio.h>
#include <math.h>
float calculate_vc(float V, float R, float C, float t) {
    return V * (1 - exp(-t / (R * C)));
}
int main()
{
    float R, C, V, t;
    printf("Enter resistance (R): ");
    scanf("%f", &R);
    printf("Enter capacitance (C): ");
    scanf("%f", &C);
    printf("Enter voltage (V): ");
    scanf("%f", &V);
    printf("Enter time (t): ");
    scanf("%f", &t);
    float Vc = calculate_vc(V, R, C, t);
    printf("Voltage across capacitor (Vc): %.2f V\n", Vc);
    return 0;
}
#include <stdio.h>
#include <math.h>
float calculate_il(float V, float R, float L, float t)
{
    return (V / R) * (1 - exp(-t / (L / R)));
}

int main()
{
    float R, L, V, t;

    printf("Enter resistance (R): ");
    scanf("%f", &R);
    printf("Enter inductance (L): ");
    scanf("%f", &L);
    printf("Enter voltage (V): ");
    scanf("%f", &V);
    printf("Enter time (t): ");
    scanf("%f", &t);

    float Il = calculate_il(V, R, L, t);

    printf("Current through inductor (Il): %.2f A\n", Il);

    return 0;
}
#include <stdio.h>
#include <math.h>

// Function to calculate power factor
float calculate_pf(float angle) {
    return cos(angle * M_PI / 180);
}

int main() {
    float angle;

    printf("Enter power factor angle (degrees): ");
    scanf("%f", &angle);

    float pf = calculate_pf(angle);

    printf("Power factor: %.2f\n", pf);

    return 0;
}
