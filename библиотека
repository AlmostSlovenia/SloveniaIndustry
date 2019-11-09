# библиотека Малков
txLine (x + 50 * s, y + 40 * s, x + 50 * s, y);
    txLine (x + 50 * s, y, x + 30 * s, y - 20 * s);
    txLine (x + 30 * s, y - 20 * s, x + 20 * s, y - 20 * s);
    txLine (x + 20 * s, y - 20 * s, x, y);
    txFloodFill (x + 1 * s, y);//zalivka


    for (int kvadratikov = 1; kvadratikov <= kolichestvo; kvadratikov++)//y prizraka est' poyas, tyt zadaetsa kolichestvo elementov poyasa
    {
        if (kvadratikov == 1) // risuem pervii element i daem emy krasnii zvet
        {
            txSetFillColor (TX_RED);
            txRectangle (x, y + 20 * s, x + 50 * s / kolichestvo, y + 30 * s);
        }
        else if (kvadratikov == kolichestvo)//risuem poslednii element i daem emy krasnii zvet
        {
            txSetFillColor (TX_RED);
            txRectangle (x + 50 * s * (kolichestvo - 1) / kolichestvo, y + 20 * s, x + 50 * s, y + 30 * s);
        }
        else
        {
            txSetFillColor (TX_DARKGRAY);//risuem ostalnie elementi poyasa
            txRectangle (x + 50 * s * (kolichestvo - kvadratikov) / kolichestvo, y + 20 * s, x + 50 * s * (kolichestvo - kvadratikov + 1) / kolichestvo, y + 30 * s);
        }

    }

    txSetFillColor (TX_GREEN);//risuem glaz prizraka
    txEllipse (x + 10 * s, y, x + 40 * s, y - 10 * s);






}
void babochka_ghost1()
{
    if(babochka1==true)//risuem babochky prizraka
    {
        txSetFillColor (TX_BLACK);
        POINT BABOCHKA[4] = {{x + 10 * s, y}, {x + 10 * s, y + 20 * s}, {x + 40 * s, y}, {x + 40 * s, y + 20 * s}};
        txPolygon (BABOCHKA, 4);
    }
}
void shlyapa_ghost1()
{

    if (shlyapa==true)
    {


        txSetFillColor (TX_BLACK);//risuem shlyapu prizraka
        txRectangle (x + 10 * s, y - 15 * s, x + 40 * s, y - 20 * s);
        txSetFillColor (TX_WHITE);
        txRectangle (x + 15 * s, y - 20 * s, x + 35 * s, y - 22 * s);
        txSetFillColor (TX_BLACK);
        txRectangle (x + 15 * s, y - 22 * s, x + 35 * s, y - 30 * s);

    }
}
void Interface()
{
    txSetFillColor (TX_BLACK);
    txRectangle(0,0,125,600);
    txSelectFont ("Comic Sans MS", 20);//risuem elementi interfeisa,minyaem shrift,
    txSetFillColor ( TX_ORANGE);

    txRectangle(5,70,120,120);
    RECT speed_button={5,70,120,120};
    txTextOut (10, 85, "I am speed!");
    txSetFillColor (TX_ORANGE);
    txRectangle(5,131,120,180);
    RECT size_button={5,131,120,180};
    txTextOut (10, 145, "I am size!");
    txSetFillColor (TX_ORANGE);
    txRectangle(5,191,120,240);
    RECT poyas_button={5,191,120,240};
    txTextOut (10, 205, "I am Poyas!");
    txSetFillColor (TX_ORANGE);
    txRectangle(5,251,120,300);
    RECT shlyapa_button={5,251,120,300};
    txTextOut (10, 265, "I am Shlaypa!");
    txSetFillColor (TX_ORANGE);
    txRectangle(5,311,120,350);
    RECT babochka_button={5,311,120,360};
    txTextOut (10, 325, "I am Babochka!");

    if(txMouseButtons() & 1)//realisuem ismenenie v polozhitelnuu storony
    {
        if(In (txMousePos(), speed_button))speed = speed+10;
        if(In (txMousePos(), size_button)) s = s+1;
        if(In (txMousePos(), poyas_button)) kolichestvo = kolichestvo+1;
        if(In (txMousePos(), shlyapa_button))shlyapa =true;
        if(In (txMousePos(), babochka_button))babochka1 =true;
    }
    if(txMouseButtons() & 2)//realisuem ismenenie v otrizatelnuu storony
    {
        if(In (txMousePos(), speed_button))speed = speed-10;
        if(In (txMousePos(), size_button)) s = s-1;
        if(In (txMousePos(), poyas_button)) kolichestvo = kolichestvo-1;
        if(In (txMousePos(), shlyapa_button))shlyapa =false;
        if(In (txMousePos(), babochka_button))babochka1 =false;
    }



}
void way1()
{
    if ( (1 < x) and (x <= 100))//risuem put' peremeshenia prizraka
        y = y + 1;
    if ( (100 < x) and (x <= 200))
        y = y - 1;




}
void full_ghost1()
{

    ghost1();//zadaem samogo prizraka iz vsex elementov
    shlyapa_ghost1();
    babochka_ghost1();

}
void background()
{
 txSetFillColor (TX_DARKGRAY);
 txRectangle(0,0,1000,6);
 txSetFillColor ( TX_LIGHTGRAY);
 txRectangle(0,300,1000,0);



}
