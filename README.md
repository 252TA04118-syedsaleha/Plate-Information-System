#include <stdio.h>

struct Plate {
    char name[50];
    char material[30];
    char shape[20];
    char color[20];
    float size;
    float price;
    int quantity;
};

int main() {
    struct Plate plate;
    float total;

    printf("============================================\n");
    printf("           PLATE INFORMATION SYSTEM         \n");
    printf("============================================\n");

    printf("\nEnter Plate Name: ");
    scanf(" %[^\n]", plate.name);

    printf("Enter Plate Material: ");
    scanf(" %[^\n]", plate.material);

    printf("Enter Plate Shape: ");
    scanf(" %[^\n]", plate.shape);

    printf("Enter Plate Color: ");
    scanf(" %[^\n]", plate.color);

    printf("Enter Plate Size (cm): ");
    scanf("%f", &plate.size);

    printf("Enter Plate Price: ");
    scanf("%f", &plate.price);

    printf("Enter Quantity: ");
    scanf("%d", &plate.quantity);

    total = plate.price * plate.quantity;

    printf("\n============================================\n");
    printf("              PLATE DETAILS                 \n");
    printf("============================================\n");

    printf("Name          : %s\n", plate.name);
    printf("Material      : %s\n", plate.material);
    printf("Shape         : %s\n", plate.shape);
    printf("Color         : %s\n", plate.color);
    printf("Size          : %.2f cm\n", plate.size);
    printf("Price         : Rs. %.2f\n", plate.price);
    printf("Quantity      : %d\n", plate.quantity);
    printf("Total Amount  : Rs. %.2f\n", total);

    printf("\n--------------------------------------------\n");
    printf("              PRICE CATEGORY               \n");
    printf("--------------------------------------------\n");

    if (plate.price < 200) {
        printf("Category: Budget Plate\n");
    }
    else if (plate.price <= 1000) {
        printf("Category: Standard Plate\n");
    }
    else {
        printf("Category: Premium Plate\n");
    }

    printf("\n--------------------------------------------\n");
    printf("                CARE TIPS                  \n");
    printf("--------------------------------------------\n");

    printf("1. Wash the plate properly after use.\n");
    printf("2. Keep the plate clean and dry.\n");
    printf("3. Handle glass and ceramic plates carefully.\n");
    printf("4. Store plates safely to prevent damage.\n");
    printf("5. Use the plate according to its material.\n");

    printf("\n============================================\n");
    printf("       Plate Information Completed!        \n");
    printf("============================================\n");

    return 0;
}
