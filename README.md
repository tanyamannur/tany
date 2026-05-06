#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fp;
    char buffer[256];

    // Replace with the path to your file in the Git repo
    fp = fopen("path/to/your/file.txt", "r");
    if (fp == NULL) {
        perror("Error opening file");
        return EXIT_FAILURE;
    }

    // Read and print file contents line by line
    while (fgets(buffer, sizeof(buffer), fp) != NULL) {
        printf("%s", buffer);
    }

    fclose(fp);
    return EXIT_SUCCESS;
}
