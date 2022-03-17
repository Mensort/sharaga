const int n = 100;
const int m = 100;
int main()
{
    setlocale(LC_ALL, "Russian");
    int arr[n][m];
    int i, j, m, n, max, min, razn = 0;
    cout << "Введиие n = ";
    cin >> n;
    cout << "Введите m = ";
    cin >> m;
    srand(time(NULL));

    for (i = 0; i < n; i++)
    {

        for (j = 0; j < m; j++)
        {
            arr[i][j] = rand() % 100 - 10;
            cout << arr[i][j] << "\t";

        }
        cout << endl;
    }
    max = arr[0][0];
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < m; j++)
        {
            if (arr[i][j] > max)
            {
                max = arr[i][j];
            }
        }
    }
    cout << endl << "Max = " << max << endl;
    system("pause");
    return 0;
}
