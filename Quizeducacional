import java.util.*;

public class QuizEducacional {

    static Scanner scanner = new Scanner(System.in);

    static HashMap<String, String> usuarios = new HashMap<>();
    static HashMap<String, Boolean> premiumStatus = new HashMap<>();
    static String usuarioLogado = "";

    public static void main(String[] args) {
        while (true) {
            System.out.println("\n=== QUIZ SOBRE ODS 3 E ODS 4 ===");
            System.out.println("1. Cadastrar");
            System.out.println("2. Login");
            System.out.println("3. Sair");
            System.out.print("Escolha: ");
            String escolha = scanner.nextLine();

            switch (escolha) {
                case "1":
                    cadastrar();
                    break;
                case "2":
                    if (login()) {
                        menuQuiz();
                    }
                    break;
                case "3":
                    System.out.println("Encerrando o programa.");
                    return;
                default:
                    System.out.println("Opção inválida.");
            }
        }
    }

    static void cadastrar() {
        System.out.print("Digite um nome de usuário: ");
        String usuario = scanner.nextLine();

        if (usuarios.containsKey(usuario)) {
            System.out.println("Usuário já existe.");
            return;
        }

        System.out.print("Digite uma senha: ");
        String senha = scanner.nextLine();

        System.out.print("Deseja ser Premium? (s/n): ");
        String premium = scanner.nextLine();

        usuarios.put(usuario, senha);
        premiumStatus.put(usuario, premium.equalsIgnoreCase("s"));

        System.out.println("Cadastro realizado com sucesso!");
    }

    static boolean login() {
        System.out.print("Usuário: ");
        String usuario = scanner.nextLine();

        System.out.print("Senha: ");
        String senha = scanner.nextLine();

        if (usuarios.containsKey(usuario) && usuarios.get(usuario).equals(senha)) {
            System.out.println("Login bem-sucedido!");
            usuarioLogado = usuario;
            return true;
        } else {
            System.out.println("Usuário ou senha incorretos.");
            return false;
        }
    }

    static void menuQuiz() {
        System.out.println("\n=== Bem-vindo, " + usuarioLogado + " ===");

        if (premiumStatus.get(usuarioLogado)) {
            System.out.println("Status: PREMIUM");
            jogarQuiz(true);
        } else {
            System.out.println("Status: COMUM");
            System.out.println("Apenas a primeira pergunta estará disponível.");
            jogarQuiz(false);
        }
    }

    static void jogarQuiz(boolean completo) {
        int pontuacao = 0;

        System.out.println("\nIniciando o Quiz sobre as ODS 3 e 4...\n");

        // Pergunta 1
        System.out.println("1. Qual é o principal objetivo da ODS 3?");
        System.out.println("a) Reduzir o consumo de energia");
        System.out.println("b) Assegurar uma vida saudável e promover o bem-estar para todos");
        System.out.println("c) Melhorar a infraestrutura de transportes");
        System.out.println("d) Promover o comércio internacional");
        System.out.print("Resposta: ");
        String resposta1 = scanner.nextLine();
        if (resposta1.equalsIgnoreCase("b")) {
            pontuacao++;
        }

        if (!completo) {
            System.out.println("\nAdquira o plano premium para jogar o quiz completo!");
            System.out.println("Sua pontuação: " + pontuacao + "/1");
            return;
        }

        // Pergunta 2
        System.out.println("\n2. O que contribui diretamente para uma boa saúde mental?");
        System.out.println("a) Privação de sono");
        System.out.println("b) Sedentarismo");
        System.out.println("c) Atividade física regular");
        System.out.println("d) Excesso de trabalho");
        System.out.print("Resposta: ");
        String resposta2 = scanner.nextLine();
        if (resposta2.equalsIgnoreCase("c")) {
            pontuacao++;
        }

        // Pergunta 3
        System.out.println("\n3. O que é um hábito saudável para a saúde cardiovascular?");
        System.out.println("a) Fumar esporadicamente");
        System.out.println("b) Comer fast food regularmente");
        System.out.println("c) Manter uma dieta equilibrada e praticar exercícios");
        System.out.println("d) Tomar energéticos diariamente");
        System.out.print("Resposta: ");
        String resposta3 = scanner.nextLine();
        if (resposta3.equalsIgnoreCase("c")) {
            pontuacao++;
        }

        // Pergunta 4
        System.out.println("\n4. Qual é um dos pilares da educação de qualidade?");
        System.out.println("a) Ensino baseado em punições");
        System.out.println("b) Acesso limitado à tecnologia");
        System.out.println("c) Formação continuada de professores");
        System.out.println("d) Exclusão de alunos com deficiência");
        System.out.print("Resposta: ");
        String resposta4 = scanner.nextLine();
        if (resposta4.equalsIgnoreCase("c")) {
            pontuacao++;
        }

        // Pergunta 5
        System.out.println("\n5. Qual é a importância da vacinação?");
        System.out.println("a) Aumentar o consumo de medicamentos");
        System.out.println("b) Promover imunidade e prevenir doenças");
        System.out.println("c) Substituir hábitos saudáveis");
        System.out.println("d) Combater a obesidade");
        System.out.print("Resposta: ");
        String resposta5 = scanner.nextLine();
        if (resposta5.equalsIgnoreCase("b")) {
            pontuacao++;
        }

        // Pergunta 6
        System.out.println("\n6. Qual ação contribui para um ambiente escolar inclusivo?");
        System.out.println("a) Segregação por nível de aprendizagem");
        System.out.println("b) Ausência de adaptações curriculares");
        System.out.println("c) Valorização da diversidade e inclusão de todos");
        System.out.println("d) Foco apenas no rendimento acadêmico");
        System.out.print("Resposta: ");
        String resposta6 = scanner.nextLine();
        if (resposta6.equalsIgnoreCase("c")) {
            pontuacao++;
        }

        // Pergunta 7
        System.out.println("\n7. Qual é um dos principais fatores para o abandono escolar?");
        System.out.println("a) Participação ativa da família");
        System.out.println("b) Acesso fácil à escola");
        System.out.println("c) Condições socioeconômicas desfavoráveis");
        System.out.println("d) Uso de tecnologias educacionais");
        System.out.print("Resposta: ");
        String resposta7 = scanner.nextLine();
        if (resposta7.equalsIgnoreCase("c")) {
            pontuacao++;
        }

        // Pergunta 8
        System.out.println("\n8. Como a educação pode impactar a saúde?");
        System.out.println("a) Não tem relação");
        System.out.println("b) Melhora a compreensão sobre prevenção de doenças");
        System.out.println("c) Leva a escolhas piores de alimentação");
        System.out.println("d) Aumenta o estresse da população");
        System.out.print("Resposta: ");
        String resposta8 = scanner.nextLine();
        if (resposta8.equalsIgnoreCase("b")) {
            pontuacao++;
        }

        System.out.println("\nQuiz finalizado! Sua pontuação: " + pontuacao + "/8");
    }
}
