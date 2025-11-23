// EXERCÍCIO 1 — TABUADA
        // ===============================

        Console.WriteLine("EXERCÍCIO 1 - TABUADA");
        Console.WriteLine("Digite um número:");
        int numero = int.Parse(Console.ReadLine());   // Lê o número digitado

        Console.WriteLine($"\nTabuada de {numero}:");

        // Laço for repetindo de 1 até 10
        for (int i = 1; i <= 10; i++)
        {
            Console.WriteLine($"{numero} x {i} = {numero * i}");
        }

        Console.WriteLine("\n-----------------------------------\n");



   
        // EXERCÍCIO 2 — VALIDAÇÃO DE NOTA
        //

        Console.WriteLine("EXERCÍCIO 2 - VALIDAÇÃO DE NOTA");

        int nota;   // Variável criada antes do DO

        // DO-WHILE roda pelo menos 1 vez
        do
        {
            Console.WriteLine("Digite uma nota entre 0 e 10:");
            nota = int.Parse(Console.ReadLine());

            if (nota < 0 || nota > 10)
            {
                Console.WriteLine("Valor inválido! Tente novamente.");
            }

        } while (nota < 0 || nota > 10); // Repete enquanto a nota for inválida

        Console.WriteLine($"Nota válida digitada: {nota}");

        Console.WriteLine("\n-----------------------------------\n");



        
        // EXERCÍCIO 3 — CONTROLE DE PESO
        // 

        Console.WriteLine("EXERCÍCIO 3 - CONTROLE DE PESO");

        int totalIdades = 0;
        int pessoasAcima90 = 0;

        // Vai repetir 7 vezes
        for (int i = 1; i <= 7; i++)
        {
            Console.WriteLine($"\nPessoa {i}:");

            Console.WriteLine("Digite a idade:");
            int idade = int.Parse(Console.ReadLine());

            Console.WriteLine("Digite o peso:");
            double peso = double.Parse(Console.ReadLine());

            totalIdades += idade;  // Soma das idades

            if (peso > 90)
            {
                pessoasAcima90++; // Conta pessoas com peso > 90
            }
        }

        // Calcula média das idades
        double mediaIdades = totalIdades / 7.0;

        Console.WriteLine($"\nQuantidade de pessoas com mais de 90 kg: {pessoasAcima90}");
        Console.WriteLine($"Média das idades das 7 pessoas: {mediaIdades}");
    }
}
