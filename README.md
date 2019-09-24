# matrix-operations
addition, subtraction, multiplication, division and transpose of matrices
 #include <iostream>
    using namespace std;
    class matrix3
    {
        int a[10][10],b[10][10],c[10][10],d[10][10],e[10][10],f[10][10],g[10][10],h[10][10],x,y,i,j;
        public :
            void values();
            void transpose();
            void sum();
            void diff();
            void multi();
            void div();
    };
    void matrix3::values()
    {
        cout << "Enter the rows   "; cin >> x;
        cout << "Enter the columns   "; cin >> y;
        cout << "Enter elements of first matrix\n";
        for (i=1; i<=x; i++)
        {
            for ( j=1; j<=y; j++)
            {
                cin >> a[i][j];
            }
        }
        cout << "Enter elements of second matrix\n";
        for (i=1; i<=x; i++)
        {
            for (j=1; j<=y; j++)
            {
                cin >> c[i][j];
            }
        }
    }
    void matrix3::sum()
    {
        cout << "Sum of Matrices 1 and 2 is\n";
        for (i=1; i<=x; i++)
        {
            for ( j=1; j<=y; j++)
            {
                e[i][j]=a[i][j]+c[i][j];
                cout << e[i][j] << "\t";
            }
            cout << endl;
        }

    }
    void matrix3::diff()

    {
    cout << "Difference of Matrices 1 and 2 (1-2) is\n";
        for (i=1; i<=x; i++)
        {
            for ( j=1; j<=y; j++)
            {
                f[i][j] = a[i][j]-c[i][j];
                cout << f[i][j] << "\t";
            }
            cout << endl;
        }
    }
    void matrix3::multi()
    {
        cout<<"multiplication of matrices 1 and 2 (1*2) is\n";
        for(i=1;i<=x;i++)
        {
            for(j=1;j<=y; j++)
            {
                g[i][j]=a[i][j]*c[i][j];
                cout<< g[i][j]<<"\t";
            }
            cout<< endl;
        }
    }
    void matrix3:: div()
    {
        cout<<"division of matrices 1 and 2 (1/2) is \n";
        for (i=1;i<=x; i++)
        {
            for(j=1; j<=y ; j++)
            {
                h[i][j]=a[i][j]/c[i][j];
                cout<< h[i][j]<<"\t";

            }
            cout<< endl;
        }
    }
    void matrix3::transpose()
    {
        cout << "transpose of the matrix is\n";
        for ( i=1; i<=x; i++)
        {
            for ( j=1; j<=y; j++)
            {
                b[i][j] = a[j][i];
                cout << b[i][j] << "\t";
            }
            cout << endl;
        }
        cout << "Transpose of the second matrix is\n";
        for ( i=1; i<=x; i++)
        {
            for ( j=1; j<=y; j++)
            {
                d[i][j] = c[j][i];
                cout << b[i][j] << "\t";
            }
            cout << endl;
        }
    }
    int main()
    {
        int input;
        char ch;
        matrix3 m;
        m.values();
        do
         {
        cout << "Enter your choice\n";
        cout << "1. Addition " << "2. Difference " << "3. Multiplication " <<"4. Division "<<"5. Transpose " ;
        cin >> input;
        switch (input)
        {
            case 1:
                m.sum();
                break;

            case 2:
                m.diff();
                break;
            case 3:
                m.multi();
                break;
            case 4:
                m.div();
                break;
            case 5:
                m.transpose();
                break;

        }
        cout << "Do another y?";
        cin >> ch;
        }
        while (ch!= 'n');
        cout << "";
   //     system ("pause");
    return 0;
    }
