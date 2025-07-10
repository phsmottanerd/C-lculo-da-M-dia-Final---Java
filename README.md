# 📊 Cálculo da Média Final - Java

Este projeto foi desenvolvido durante meus estudos no **curso Java Development de 60 horas da FIAP**, como parte do aprendizado de lógica de programação e manipulação de dados com entrada pelo teclado.

---

## 🧠 Sobre o Projeto

O objetivo do programa é calcular a **média final de um aluno**, com base em:
- **Prova Semestral (50%)**
- **Trabalho de Conclusão de Curso (30%)**
- **Duas Provas Intermediárias (20%)**

O sistema solicita os dados do usuário pelo terminal e aplica regras de decisão para informar se o aluno:
✅ Está aprovado  
⚠️ Está de exame  
❌ Está reprovado

---

## 💻 Ferramentas e Tecnologias Utilizadas

### ☕ Java  
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg" alt="Java" width="100" />

- Linguagem principal usada no projeto.
- Aplicação de estruturas básicas como variáveis, entrada de dados e condicionais.

### 🧠 Minha Dedicação
- Estou focado na minha transição de carreira com disciplina e esforço diário.
- Pratico exercícios como este para evoluir como desenvolvedor Java júnior.

### 🧠 IDE: IntelliJ IDEA  
<img src="https://resources.jetbrains.com/storage/products/intellij-idea/img/meta/intellij-idea_logo_300x300.png" alt="IntelliJ IDEA" width="80" />

- Ambiente utilizado para desenvolver, compilar e testar o código com eficiência.

---

## 📌 O que aprendi neste projeto:
- Entrada de dados com `Scanner`
- Operações com `float` e `double`
- Cálculo de média ponderada
- Uso de condicionais (`if`, `else if`, `else`)
- Escrita e organização de código limpo e comentado

---

## 📦 Código-Fonte

```java
import java.util.Scanner;

class Main {
    /**
     * A) Prova semestral que compõe 50% da média;
     * B) Trabalho de conclusão de curso que possui 30%;
     * C) As avaliações intermediárias, que são compostas por duas avaliações.
     * 20% para a média final.
     */
    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        System.out.println("Informe a nota da prova semestral:");
        float ps = entrada.nextFloat();

        System.out.println("Informe a nota do TCC:");
        float tcc = entrada.nextFloat();

        System.out.println("Informe a nota da Prova Intermediária 1:");
        float av1 = entrada.nextFloat();

        System.out.println("Informe a nota da Prova Intermediária 2:");
        float av2 = entrada.nextFloat();

        double mediaFinal = ps * 0.5 + tcc * 0.3 + ((av1 + av2) / 2) * 0.2;

        System.out.println("A média final é: " + mediaFinal);

        if (mediaFinal >= 6)
            System.out.println("✅ Aprovado");
        else if (mediaFinal >= 3)
            System.out.println("⚠️ Está de exame");
        else
            System.out.println("❌ Está reprovado");
    }
}
