linha 158 não pode ser:

// Enviar resposta completa para o email do administrador (sem o utilizador ver)
emailjs.send("service_j185cn5", "template_hl5w2it", {
  message: gerarRelatorioCompleto()
});

function gerarRelatorioCompleto() {
  let relatorio = "Novo resultado do Quiz Confissões a Dois:\n\n";

  for (let i = 0; i < results.length; i++) {
    const pergunta = questions[i].question;
    const resposta = results[i].text;
    relatorio += `Pergunta ${i + 1}: ${pergunta}\nResposta: ${resposta}\n\n`;
  }

  return relatorio;
}
