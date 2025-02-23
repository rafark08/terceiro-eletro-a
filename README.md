<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Alunos - Eletro 2023 A</title>
<style>
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    overflow-x: hidden;
    background: #2c3e50; /* Fundo azul-escuro moderno */
}
.section {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    position: relative;
}
.intro {
    position: relative;
    overflow: hidden;
    color: white;
    font-size: 3em;
    font-weight: bold;
    padding: 0 20px;
}
.background-image {
    background: url('https://i.imgur.com/vSW9Z9e.jpg') no-repeat center center fixed;
    background-size: cover;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 0;
    transition: filter 0.3s ease;
}
.intro-text {
    position: relative;
    z-index: 1;
    font-size: 4em;
    margin: 0;
    opacity: 0;
    transition: opacity 2s ease-in;
    text-shadow: 2px 2px 4px #000; /* Adiciona contorno preto */
}

/* Media Queries para dispositivos móveis e tablets */
@media (max-width: 768px) {
    .intro-text {
        font-size: 2.5em; /* Ajuste para tablets */
    }
}

@media (max-width: 480px) {
    .intro-text {
        font-size: 2em; /* Ajuste para celulares */
        line-height: 1.2; /* Ajuste de altura da linha para celulares */
    }
}
.students {
    background: rgba(0, 0, 0, 0.5); /* Fundo semitransparente para a sessão dos alunos */
    backdrop-filter: blur(5px); /* Aplicando blur na sessão dos alunos */
    padding: 20px;
    border-radius: 10px;
    margin-top: -10px;
    text-align: left;
}
.students h2 {
    display: none; /* Remover o título "Nossa Turma" */
}
.students p {
    display: none; /* Remover o parágrafo "Bem-vindo..." */
}
.container {
    width: 100%;
    max-width: 1000px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    padding: 20px;
    background: transparent; /* Alterar fundo para transparente */
    border-radius: 10px;
}
/* Estilos gerais para os alunos */
.aluno {
    color: white;
    padding: 20px;
    margin: 10px;
    border-radius: 10px;
    width: 200px;
    height: 300px;
    transition: all 0.5s ease;
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    position: relative;
    overflow: hidden;
    cursor: pointer;
    background-color: #6a89cc;
}

.aluno:hover {
    box-shadow: 0 12px 20px rgba(0, 0, 0, 0.2);
    transform: translateY(-5px);
}

/* Estilos personalizados para as imagens de fundo */
.aluno.julia::before {
    content: '';
    background: url('https://imgur.com/EiwHqfO.jpg') no-repeat center center;
    background-size: cover;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0.3;
    transition: opacity 0.5s ease;
    z-index: 0;
}

.aluno.nicolas::before {
    content: '';
    background: url('https://imgur.com/7tz9xje.jpg') no-repeat center center;
    background-size: cover;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0.3;
    transition: opacity 0.5s ease;
    z-index: 0;
}

.aluno.raissa::before {
    content: '';
    background: url('https://imgur.com/37t33RP.jpg') no-repeat center center;
    background-size: cover;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0.3;
    transition: opacity 0.5s ease;
    z-index: 0;
}

.aluno:hover::before {
    opacity: 1;
}
.aluno h3 {
    font-size: 18px;
    margin-bottom: 5px;
    font-weight: bold; /* Texto em negrito */
    text-transform: uppercase;
    letter-spacing: 1px;
    position: relative;
    background-color: rgba(0, 0, 0, 0.4); /* Caixa de fundo */
    padding: 10px;
    border-radius: 10px;
    display: inline-block;
    z-index: 1;
    white-space: normal; /* Permite quebra de linha */
    word-break: break-word; /* Quebra de linha dentro da palavra, se necessário */
    text-shadow: 1px 1px 2px #000; /* Adiciona contorno preto aos nomes dos alunos */
    
}


/* Outros estilos gerais... */

/* Degradês personalizados para cada aluno */
.airha {
    background: linear-gradient(145deg, #ff9a9e, #fad0c4); /* Degradê suave rosa e bege */
}
.bruna {
    background: linear-gradient(145deg, #ff6a00, #ee0979); /* Gradiente laranja e rosa */
}
.bruno {
    background: linear-gradient(145deg, #fbc2eb, #a6c1ee); /* Degradê rosa e azul claro */
}
.daniel {
    background: linear-gradient(145deg, #fc466b, #3f5efb); /* Gradiente rosa e azul */
}
.eduardo {
    background: linear-gradient(145deg, #84fab0, #8fd3f4); /* Degradê verde e azul claro */
}
.elliel {
    background: linear-gradient(145deg, #a18cd1, #fbc2eb); /* Degradê roxo e rosa */
}
.estefani {
    background: linear-gradient(145deg, #ff758c, #ff7eb3); /* Degradê vermelho e rosa */
}
.fernanda {
    background: linear-gradient(145deg, #ff9a9e, #fecfef); /* Degradê rosa claro */
}
.gabriel {
    background: linear-gradient(145deg, #a1c4fd, #c2e9fb); /* Degradê azul claro */
}
.henrique {
    background: linear-gradient(145deg, #f6d365, #fda085); /* Degradê laranja e amarelo */
}
.igor {
    background: linear-gradient(145deg, #ffdde1, #ee9ca7); /* Degradê rosa claro */
}
.isadora {
    background: linear-gradient(145deg, #f093fb, #f5576c); /* Degradê roxo e vermelho */
}
.julia {
    background: linear-gradient(145deg, #e0c3fc, #8ec5fc); /* Degradê roxo e azul */
}
.laura {
    background: linear-gradient(145deg, #fbc2eb, #a18cd1); /* Degradê rosa e roxo */
}
.leticia {
    background: linear-gradient(145deg, #f6d365, #fda085); /* Degradê laranja e amarelo */
}
.luiza {
    background: linear-gradient(145deg, #f093fb, #f5576c); /* Degradê roxo e vermelho */
}
.maria {
    background: linear-gradient(145deg, #a1c4fd, #c2e9fb); /* Degradê azul claro */
}
.matheus {
    background: linear-gradient(145deg, #84fab0, #8fd3f4); /* Degradê verde e azul claro */
}
.matheusm {
    background: linear-gradient(145deg, #ff9a9e, #fad0c4); /* Degradê suave rosa e bege */
}
.nicolas {
    background: linear-gradient(145deg, #fbc2eb, #a6c1ee); /* Degradê rosa e azul claro */
}
.rafael {
    background: linear-gradient(145deg, #00d2ff, #3a47d5); /* Gradiente azul */
}
.raissa {
    background: linear-gradient(145deg, #ff758c, #ff7eb3); /* Degradê vermelho e rosa */
}
.thiago {
    background: linear-gradient(145deg, #a18cd1, #fbc2eb); /* Degradê roxo e rosa */
}
.tiago {
    background: linear-gradient(145deg, #f6d365, #fda085); /* Degradê laranja e amarelo */
}
.tiagod {
    background: linear-gradient(145deg, #e0c3fc, #8ec5fc); /* Degradê roxo e azul */
}
.vinicius {
    background: linear-gradient(145deg, #ffdde1, #ee9ca7); /* Degradê rosa claro */
}

/* Outros estilos específicos... */
.aluno h3 {
    font-size: 18px;
    margin-bottom: 5px;
    font-weight: bold; /* Texto em negrito */
    text-transform: uppercase;
    letter-spacing: 1px;
    position: relative;
    background-color: rgba(0, 0, 0, 0.4); /* Caixa de fundo */
    padding: 10px;
    border-radius: 10px;
    display: inline-block;
    z-index: 1;
    white-space: normal; /* Permite quebra de linha */
    word-break: break-word; /* Quebra de linha dentro da palavra, se necessário */
    text-shadow: 1px 1px 2px #000; /* Adiciona contorno preto aos nomes dos alunos */
}

.info {
    opacity: 0;
    transition: opacity 0.3s ease-in-out;
    margin-top: 5px;
    font-size: 14px;
    letter-spacing: 0.5px;
    line-height: 1.4;
    white-space: nowrap;
    position: relative;
    z-index: 1;
    padding: 10px;
    backdrop-filter: blur(8px); /* Aplicando blur diretamente */
    background: rgba(0, 0, 0, 0.3); /* Cor de fundo com opacidade */
    border-radius: 10px; /* Bordas arredondadas para o fundo com blur */
}
.aluno:hover .info {
    opacity: 1;
}
.aluno h3, .info {
    transition: all 0.3s ease;
}
.aluno:hover h3 {
    color: #ffffff; /* Texto branco */
    font-size: 20px; /* Tamanho maior da fonte */
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8); /* Sombra preta com opacidade */
    font-weight: bold; /* Texto em negrito */
}
.aluno::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0); /* Removendo a cor de fundo */
    z-index: 0;

}

/* Estilos específicos para os alunos */
.bruna {
    background: linear-gradient(145deg, #ff6a00, #ee0979); /* Gradiente laranja e rosa */
    background-size: cover;
}
.daniel {
    background: linear-gradient(145deg, #fc466b, #3f5efb); /* Gradiente rosa e azul */
    background-size: cover;
}
.rafael {
    background: linear-gradient(145deg, #00d2ff, #3a47d5); /* Gradiente azul */
    background-size: cover;
}
/* Estilos para o nome completo e primeiro nome */
.aluno h3 .full-name {
    display: none;
}
.aluno h3 .first-name {
    display: inline;
}
.aluno:hover h3 .full-name {
    display: inline;
}
.aluno:hover h3 .first-name {
    display: none;
}
/* Ajuste para aumentar o retângulo ao exibir o nome completo */
.aluno {
    transition: width 0.3s ease, height 0.3s ease;
}
.aluno:hover {
    width: 250px; /* Aumenta a largura */
    height: 350px; /* Aumenta a altura */
}
</style>
</head>
<body>
<div class="section intro">
    <div class="background-image" id="background-image"></div>
    <h1 class="intro-text" id="intro-text">
        TERCEIRÃO<br>
        ELETRO A
    </h1>
</div>
<div class="section students">
    <div class="container">
        <!-- Alunos com datas de nascimento -->
        <div class="aluno airha" data-birthdate="2007-06-10">
            <h3>
                <span class="first-name">Airha</span>
                <span class="full-name">Airha dos Santos Salviano</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno bruna" data-birthdate="2007-12-18">
            <h3>
                <span class="first-name">Bruna</span>
                <span class="full-name">Bruna Consoni Rech</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno bruno" data-birthdate="2008-03-28">
            <h3>
                <span class="first-name">Bruno</span>
                <span class="full-name">Bruno Batista</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno daniel" data-birthdate="2007-11-12">
            <h3>
                <span class="first-name">Daniel</span>
                <span class="full-name">Daniel Zonta Reginato</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno eduardo" data-birthdate="2007-08-11">
            <h3>
                <span class="first-name">Eduardo</span>
                <span class="full-name">Eduardo Simionatto</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno elliel" data-birthdate="2007-05-29">
            <h3>
                <span class="first-name">Elliel</span>
                <span class="full-name">Elliel Raimundo Barroso de Lima</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno estefani" data-birthdate="2007-10-04">
            <h3>
                <span class="first-name">Estefani</span>
                <span class="full-name">Estefani Pasqual</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno fernanda" data-birthdate="2007-02-11">
            <h3>
                <span class="first-name">Fernanda</span>
                <span class="full-name">Fernanda Massoco</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno gabriel" data-birthdate="2007-03-13">
            <h3>
                <span class="first-name">Gabriel</span>
                <span class="full-name">Gabriel Maciel Moresco</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno henrique" data-birthdate="2008-05-12">
            <h3>
                <span class="first-name">Henrique</span>
                <span class="full-name">Henrique Chaicoski</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno igor" data-birthdate="2007-08-20">
            <h3>
                <span class="first-name">Igor</span>
                <span class="full-name">Igor Colasso Trindade</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno isadora" data-birthdate="2007-09-20">
            <h3>
                <span class="first-name">Isadora</span>
                <span class="full-name">Isadora das Chagas Rettore</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno julia" data-birthdate="2007-11-08">
            <h3>
                <span class="first-name">Julia</span>
                <span class="full-name">Julia Gabriele Pereira</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno laura" data-birthdate="2007-04-11">
            <h3>
                <span class="first-name">Laura</span>
                <span class="full-name">Laura Sônego Gomes de Magalhães</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno leticia" data-birthdate="2007-06-14">
            <h3>
                <span class="first-name">Leticia</span>
                <span class="full-name">Leticia Massignani Gonçalves</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno luiza" data-birthdate="2007-06-16">
            <h3>
                <span class="first-name">Luiza</span>
                <span class="full-name">Luiza Ribeiro dos Santos</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno maria" data-birthdate="2007-08-17">
            <h3>
                <span class="first-name">Maria</span>
                <span class="full-name">Maria Eduarda Todero</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno matheus" data-birthdate="2008-03-17">
            <h3>
                <span class="first-name">Matheus</span>
                <span class="full-name">Matheus Koop</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno matheusm" data-birthdate="2007-10-03">
            <h3>
                <span class="first-name">Matheus</span>
                <span class="full-name">Matheus Macedo Danielli</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno nicolas" data-birthdate="2007-08-27">
            <h3>
                <span class="first-name">Nicolas</span>
                <span class="full-name">Nicolas Augusto de Oliveira</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno rafael" data-birthdate="2008-01-23">
            <h3>
                <span class="first-name">Rafael</span>
                <span class="full-name">Rafael Vieira de Almeida</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno raissa" data-birthdate="2007-11-09">
            <h3>
                <span class="first-name">Raissa</span>
                <span class="full-name">Raissa Waltrick Salmoria</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno thiago" data-birthdate="2007-10-17">
            <h3>
                <span class="first-name">Thiago</span>
                <span class="full-name">Thiago Jose Fresqui</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno tiago" data-birthdate="2007-06-28">
            <h3>
                <span class="first-name">Tiago</span>
                <span class="full-name">Tiago de Oliveira Jombra</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno tiagod" data-birthdate="2007-10-01">
            <h3>
                <span class="first-name">Tiago</span>
                <span class="full-name">Tiago de Siqueira Demori</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
        <div class="aluno vinicius" data-birthdate="2007-09-20">
            <h3>
                <span class="first-name">Vinicius</span>
                <span class="full-name">Vinicius Ugolini Rigo</span>
            </h3>
            <div class="info">Idade: <span class="age"></span> anos <br> Curso: Eletroeletrônica <br> Hobby: XXX</div>
        </div>
    </div>
</div>
<script>
document.addEventListener("DOMContentLoaded", function() {
    // Função para calcular a idade
    function calculateAge(birthdate) {
        const today = new Date();
        const birthDate = new Date(birthdate);
        let age = today.getFullYear() - birthDate.getFullYear();
        const monthDifference = today.getMonth() - birthDate.getMonth();
        if (monthDifference < 0 || (monthDifference === 0 && today.getDate() < birthDate.getDate())) {
            age--;
        }
        return age;
    }

    // Atualizar a idade de cada aluno
    document.querySelectorAll('.aluno').forEach(aluno => {
        const birthdate = aluno.getAttribute('data-birthdate');
        const ageElement = aluno.querySelector('.age');
        if (birthdate && ageElement) {
            const age = calculateAge(birthdate);
            ageElement.textContent = age;
        }
    });

    // Efeito de introdução
    setTimeout(function() {
        document.getElementById("background-image").style.filter = "blur(8px)";
        document.getElementById("intro-text").style.opacity = "1";

        // Lista de fontes
        const fonts = [
            "Arial",
            "Arial Italic",
            "Comic Sans MS",
            "Calibri",
            "Lucida Handwriting",
            "Impact",
            "Verdana",
            "Times New Roman Italic",
            "Courier New",
            "Tahoma"
        ];

        let currentIndex = 0;
        const introText = document.getElementById("intro-text");

        // Função para trocar a fonte
        function changeFont() {
            introText.style.fontFamily = fonts[currentIndex];
            currentIndex = (currentIndex + 1) % fonts.length;
        }

        // Trocar fonte a cada 2 segundos
        setInterval(changeFont, 1000);
    }, 3000); // Espera de 3 segundos
});
</script>
</body>
</html>
