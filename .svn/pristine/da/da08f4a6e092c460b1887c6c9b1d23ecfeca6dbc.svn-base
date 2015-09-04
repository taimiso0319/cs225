#include "png.h"

using namespace std;

PNG rotateImage(PNG original)
{
    RGBAPixel imageColor;
    int width = original.width();
    int height = original.height();
    PNG tempImage(width,height);
    //test//
    /*
    imageColor.red = 255;
    imageColor.blue = 0;
    imageColor.green = 0;
    imageColor.alpha = 255;
    */
    for(int i = 0; i < width; i++)
    {
        for(int j = 0; j < height; j++)
        {
            //*tempImage(i, j) = imageColor; //original(i,j);
            imageColor = *original(i,j);
            *tempImage(width - i - 1, height - j -1) = imageColor;
            cout << i << "" << j << endl;
        }
    }
    return tempImage;
}

int main()
{
    PNG image("in.png");
    PNG overlay("overlay.png");

    image = rotateImage(image);
    image.writeToFile("output.png");

    return 0;
}
