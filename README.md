# Clipagem Sirena

Site estático da clipagem de imprensa do Grupo Sirena (Dody Sirena, Jaime Sirena, Grupo Sirena, Sirena Gramado, Club Med Gramado, Sirena Ceará), publicado na Netlify.

- `index.html` — a página (filtros por assunto, período, veículo, busca; ordem cronológica; exportação CSV).
- `materias.json` — base do acervo.
- `novas.json` — acréscimos feitos pela varredura diária do Claude (mesclados com a base ao abrir a página). De tempos em tempos são incorporados à base.
- `netlify.toml` — publicação da raiz, sem build; JSON sem cache.

Formato de cada matéria: `{id, url, titulo, veiculo, data (YYYY-MM-DD), dataAprox, resumo, assuntos[], origem, adicionadoEm, verificada}`.
O `id` é "m" + FNV-1a 32 bits (hex, 8 dígitos) da URL normalizada (sem query/hash, sem barra final, minúsculas).
