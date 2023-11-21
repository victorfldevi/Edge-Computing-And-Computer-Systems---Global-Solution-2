# Edge-Computing-And-Computer-Systems---Global-Solution-2

Integrantes:

 - Lorenzo Gomes Andreata - RM 551117
 - Victor Flávio Demarchi Viana - RM 99389


Descrição do Problema:

	Quedas podem gerar diversos problemas para qualquer pessoa, porém são intensificadas para pessoas idosas ou que possuem alguma dificuldade de locomoção, já que por seus corpos serem mais frágeis podem ter consequencias mais severas devido ao impacto, ou mesmo não conseguir se levantar após isso, necessitando que alguém os levante.

Visão Geral:

	Um dispositivo IoT vestível (no peito do pé) que permite detectar quando seu usuário caiu no chão, através de um giroscópio e um acelerômetro, e chamar ajuda automaticamente através da internet, usando um esp32.

Instruções:

Acesso:

	Primeiramente, se deve abrir o site do simulador chamado Wokwi, através do link abaixo:

- https://wokwi.com/projects/381855169899866113

	Outra opção é baixar os arquivos presentes no repositório e, na aba "sketch.ino", copiar e colar o conteúdo presente no arquivo "Code.txt", na aba "diagram.json", copiar e colar o conteúdo presente no arquivo "Json.txt", na aba "Library Manager", copiar cada linha do conteúdo presente no arquivo "Libraries.txt", clicar no "+" em "Project Libraries", colar e selecionar a biblioteca com o mesmo nome do conteúdo colado.

	Usando qualquer um dos metodos, você terá uma cópia exata do protótipo desenvolvido para demonstrar a idéia.


Uso:

	O protótipo é capaz de detectar 3 tipos de informação, rotação e aceleração e temperatura (porém somente rotação e aceleração serão utilizados), que podem ser livremente modificados.

	Caso qualquer um dos medidores de aceleração for maior que 5 cm/s², o led de aceleração irá acender, dizendo que a pessoa está se movendo rápido (ou caindo rápido)

	Caso qualquer um dos medidores de rotação for maior que 30°, o led de rotação irá acender, dizendo que a pessoa não está de pé (ou caindo).

	Caso ambos os leds estejam ativos ao mesmo tempo, o alarme(buzzer) irá tocar, e o dispositivo esp32 chamará ajuda via wi-fi. Os leds não apagarão até que o botão reset seja pressionado por tempo o suficiente.

	Porém, através da aceleração, também podemos medir a distância da pessoa em relação ao ponto inicial, e caso o pé contendo o sensor esteja a mais de 30° de rotação, mas também esteja a uma altura de mais de 1 metro de onde ele estava antes, o sensor ligará o led verde, que indica que a pessoa está segura e não ira cair.

	Caso a pessoa esteja de pé numa altura menor ou maior de quando ligou o sensor por mais de 10 segundos, o sensor consierará a atual altura como sendo a altura do chão.
