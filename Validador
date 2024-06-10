
	    function ValidarCPF(strCPF) {
			  var Soma;
			  var Resto;
			  strCPF = strCPF.replace(/\D/g, ''); // Permite apenas números
			  Soma = 0;
			  if (strCPF == "/^(([0-9]{3}.[0-9]{3}.[0-9]{3}-[0-9]{2})|([0-9]{11}))$/") return false;

			  for (i = 1; i <= 9; i++) Soma = Soma + parseInt(strCPF.substring(i - 1, i)) * (11 - i);
			  Resto = (Soma * 10) % 11;

			  if ((Resto == 10) || (Resto == 11)) Resto = 0;
			  if (Resto != parseInt(strCPF.substring(9, 10))) return false;

			  Soma = 0;
			  for (i = 1; i <= 10; i++) Soma = Soma + parseInt(strCPF.substring(i - 1, i)) * (12 - i);
			  Resto = (Soma * 10) % 11;

			  if ((Resto == 10) || (Resto == 11)) Resto = 0;
			  if (Resto != parseInt(strCPF.substring(10, 11))) return false;
			  return true;
		}
	
		$(document).ready(function() {
			  $("#cpf").blur(function() {
				var teste = ValidarCPF($(this).val());
				$("#resposta").html((teste ? 'Válido' : 'Inválido'));
				if (teste) {
				} else {
				  alert("O campo CPF é inválido! Preencha com um CPF válido por favor.");
				  return false;
				}
			  });
		});

	  
