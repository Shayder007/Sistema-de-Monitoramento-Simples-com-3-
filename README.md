# Sistema-de-Monitoramento-Simples-com-3-
Descrição do Sistema:
# Tarefa 1 (Leitura do Botão):
Essa tarefa será responsável por simular a leitura de um botão. Ela será executada periodicamente, a cada 100ms, e enviará o estado do botão para a próxima tarefa.
# Tarefa 2 (Processamento do Botão):
Receberá o estado do botão da Tarefa 1. Caso o botão seja pressionado (simulado com a variável), ela acionará a próxima tarefa (a de controlar o LED). Caso contrário, apenas aguardará o próximo ciclo de leitura.
# Tarefa 3 (Controle do LED):
Controlará um LED (simulado como uma variável ou saída digital). Se o botão for pressionado, o LED será aceso, caso contrário, será apagado. A tarefa será executada sempre que for acionada pela Tarefa 2.
# Detalhamento da Implementação:
Definições de variáveis:
Defina variáveis para armazenar o estado do botão e do LED.
Utilize filas ou variáveis globais para compartilhar o estado entre as tarefas.
Criação das tarefas no FreeRTOS:
Tarefa 1: Leitura do botão (criada com uma prioridade baixa, executada a cada 100ms).
Tarefa 2: Processamento e decisão (executada dependendo do estado do botão).
Tarefa 3: Controle do LED (executada apenas quando acionada pela Tarefa 2).
Sincronização entre as tarefas:
Pode-se usar semáforos ou filas para que as tarefas se comuniquem e cooperem entre si.
A Tarefa 2 pode enviar um sinal para a Tarefa 3 quando detectar o estado do botão.
