# MinhaPrimeiraPagina
1° aplicação web ASP.NET Web que usa o framework Bootstrap 5 para o layout e estilo.
1. Criar o repositório no GitHub com nome: MinhaPrimeiraPagina
2. Criação do Projeto
• Abra o PowerShell ou Prompt e execute o comando abaixo:
dotnet new web -n MinhaPrimeiraPagina
cd MinhaPrimeiraPagina

• new – Cria um novo projeto;
• web – Determina como será a estrutura do projeto;
• -n – Parâmetro que determina o nome do projeto.
3. Criar a pasta: MinhaPrimeiraPagina /wwwroot
4. Criar o arquivo: index.html
![image](https://github.com/user-attachments/assets/1e514dc5-2b1b-4d5e-a574-03254d3e1079)

5. Criar o arquivo: sobre.html
![image](https://github.com/user-attachments/assets/d1f54910-2aae-497b-afa4-0333bb7565c3)

6. Adicione o conteúdo abaixo no arquivo: MinhaPrimeiraPagina /Program.cs

''app.UseDefaultFiles(); // Serve index.html por padrão
app.UseStaticFiles(); // Permite servir arquivos da pasta wwwroot''

7. Determinar que o arquivo index.html seja o padrão, portanto, o bloco de
código abaixo no dentro do arquivo: MinhaPrimeiraPagina /Program.cs

''app.MapGet("/sobre", async context =>
{
await context.Response.SendFileAsync("wwwroot/sobre.html");
});''

Estrutura esperada:
![image](https://github.com/user-attachments/assets/c149dad9-9923-4501-8017-8804974b8240)

Para executar o site através do terminal PowerShell ou Prompt execute o
comando: **dotnet run**

## Tarefa
Personalize o conteúdo da página "Sobre Mim":
• Adicione seu nome
• Escreva uma breve bio
• Adicione uma imagem com Bootstrap (<img class="img-fluid rounded">)
• Use ao menos 1 componente Bootstrap (alert, botão, card, etc.)
Não esquecer de criar um repositório com o nome MinhaPrimeiraPagina e
compartilhar o link no Classroom
