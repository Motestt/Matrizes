# Matrizes        

{
            //linhas e colunas

            Console.Write("linhas:");
            int N = int.Parse(Console.ReadLine());
            Console.Write("Colunas");
            int M = int.Parse(Console.ReadLine());

            //Matriz  

            int[,] mat = new int[N, M];



            Console.WriteLine("Digite:");

            //Entrada de dados:

            for (int i = 0; i < N; i++)
            {
                string[] values = Console.ReadLine().Split(' ');

                for (int j = 0; j < M; j++)
                {
                    mat[i, j] = int.Parse(values[j]);

                }

            }

            //logica

            int z = int.Parse(Console.ReadLine());

            for (int i = 0; i < M; i++)
            {
                for (int j = 0; j < N; j++)
                {
                    if (mat[i, j] == z)
                    {
                        Console.WriteLine("Position " + i + "," + j + ":");
                        if (j > 0)
                        {
                            Console.WriteLine("Left: " + mat[i, j - 1]);
                        }
                        if (i > 0)
                        {
                            Console.WriteLine("Up: " + mat[i - 1, j]);
                        }
                        if (j < N - 1)
                        {
                            Console.WriteLine("Right: " + mat[i, j + 1]);
                        }
                        if (i < M - 1)
                        {
                            Console.WriteLine("Down: " + mat[i + 1, j]);
                        }
                    }
                }
            }

            Console.ReadLine();

        }  
        

          }

                           

}
