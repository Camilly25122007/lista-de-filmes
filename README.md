let campoIdade;
let campoFantasia;

function setup() {
    createCanvas(400, 400);
    campoIdade = createInput("15");
    campoFantasia = createCheckbox("Gosta de Fantasia ?");
}


function draw() {
    background(220);
    let idade = campoIdade.value();
    let gostaDeFantasia = campoFantasia.checked();
    let recomendacao = geraRecomendacao(idade, gostaDeFantasia);
    text(recomendacao, width / 2, height / 2);
}

function geraRecomendacao(idade, gostaDeFantasia) {
    if(idade >= 10) {
        if(idade >= 14) {
            return "she hulk";
        } else {
            if(gostaDeFantasia){
                return "como eu era antes de você";
            } else {
                return "esquadrão suicida";
            }
        }
    } else {
        if(gostaDeFantasia) {
            return "meninas malvadas";
        } else {
            return "um espião e meio";
        }
    }
}
