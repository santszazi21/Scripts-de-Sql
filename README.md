Uso técnico do JSONB, constraints e índices

O campo prontuario foi implementado como JSONB para permitir armazenamento flexível e dinâmico de informações médicas específicas (ex.: alergias, histórico, observações).
Isso é útil quando:

os campos variam de paciente para paciente;

há integração com formulários dinâmicos ou APIs heterogêneas;

não é viável criar colunas fixas para cada tipo de dado.

 Vantagens:

Estrutura adaptável;

Permite consultas por chave (prontuario ->> 'alergias');

Facilita integração com sistemas externos.

Riscos 

Performance degradada em grandes volumes sem índices GIN;


Consultas complexas e menos otimizadas;

Dificuldade em aplicar constraints em campos internos.
