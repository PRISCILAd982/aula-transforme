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

// EXERCÍCIO 1 – Validação de Senha
        // ================================
        Console.WriteLine("=== EXERCÍCIO 1 – VALIDAÇÃO DE SENHA ===");

        string senhaCorreta = "12345";
        int tentativas = 3;
        bool acessoLiberado = false;

        for (int i = 1; i <= tentativas; i++)
        {
            Console.WriteLine("Digite a senha:");
            string senhaDigitada = Console.ReadLine();

            if (senhaDigitada == senhaCorreta)
            {
                Console.WriteLine("Informe sua idade:");
                int idade = int.Parse(Console.ReadLine());

                if (idade >= 18)
                {
                    Console.WriteLine("Acesso liberado! ");
                    acessoLiberado = true;
                    break;
                }
                else
                {
                    Console.WriteLine("Acesso negado! Você precisa ter mais de 18 anos.");
                    break;
                }
            }
            else
            {
                Console.WriteLine("Senha incorreta!");
                Console.WriteLine($"Tentativas restantes: {tentativas - i}");
            }
        }

        if (!acessoLiberado)
        {
            Console.WriteLine("Acesso bloqueado. Número de tentativas excedido ");
        }

        Console.WriteLine();
        Console.WriteLine("Aperte ENTER para continuar para o Exercício 2...");
        Console.ReadLine();

        // ==========================================
        // EXERCÍCIO 2 – Números Pares e Ímpares
        // ==========================================
        Console.WriteLine("=== EXERCÍCIO 2 – NÚMEROS PARES E ÍMPARES ===");

        Console.WriteLine("Digite um número inteiro positivo:");
        int numero = int.Parse(Console.ReadLine());

        for (int i = 1; i <= numero; i++)
        {
            if (i % 2 == 0) // par
            {
                if (i % 5 == 0) // múltiplo de 5
                {
                    Console.WriteLine($"{i} - Par e múltiplo de 5 ");
                }
                else
                {
                    Console.WriteLine($"{i} - Par");
                }
            }
            else
            {
                Console.WriteLine($"{i} - Ímpar");
            }
        }

        Console.WriteLine();
        Console.WriteLine("Aperte ENTER para continuar para o Exercício 3...");
        Console.ReadLine();

        // ====================================
        // EXERCÍCIO 3 – Caixa Registradora
        // ====================================
        Console.WriteLine("=== EXERCÍCIO 3 – CAIXA REGISTRADORA ===");

        double totalCompra = 0;
        string cupom;

        while (true)
        {
            Console.WriteLine("Digite o valor do produto (ou 0 para encerrar):");
            double valor = double.Parse(Console.ReadLine());

            if (valor == 0)
                break;

            totalCompra += valor;
        }

        Console.WriteLine($"Total da compra: R$ {totalCompra:F2}");

        Console.WriteLine("Digite um cupom de desconto (ou deixe vazio):");
        cupom = Console.ReadLine();

        if (totalCompra > 100 || cupom == "CUPOM10")
        {
            double desconto = totalCompra * 0.10;
            double totalFinal = totalCompra - desconto;

            Console.WriteLine($"Desconto aplicado: R$ {desconto:F2}");
            Console.WriteLine($"Total final: R$ {totalFinal:F2} ");
        }
        else
        {
            Console.WriteLine("Nenhum desconto aplicado.");
            Console.WriteLine($"Total final: R$ {totalCompra:F2}");
        }

        Console.WriteLine("=== FIM DO PROGRAMA ===");
    }
}


---


