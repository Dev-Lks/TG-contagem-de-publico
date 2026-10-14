# Operação — Contador de Público (uso interno)

## Enviar para o Tomazeli

Tomazeli, segue o contador de público:

**Link pros atiradores:**
https://apoiotgfiemg.vercel.app

**Cada atirador:**
1. Abre o link no celular
2. Seleciona o nome e o portão
3. Aperta +1 ENTRADA ou +1 SAÍDA conforme o movimento
4. Se errar, aperta Desfazer
5. Se ficar sem internet, continua contando — sincroniza sozinho depois

**Painel da diretoria (não mandar pros atiradores):**
https://apoiotgfiemg.vercel.app/?painel

Nele você vê público presente, entradas/saídas, fluxo por hora, movimento por portão, lista da equipe e exportação CSV/JSON.

**Pra adicionar atirador ou portão (PowerShell no PC):**
```powershell
$body = @{ password = 'SUA_SENHA'; action = 'add_person'; name = 'Atdr 120 NOME'; role = 'Atirador' } | ConvertTo-Json
Invoke-RestMethod -Method Post -Uri 'https://apoiotgfiemg.vercel.app/api/admin' -ContentType 'application/json' -Body $body

$body = @{ password = 'SUA_SENHA'; action = 'add_gate'; gate = 'Nome do portão' } | ConvertTo-Json
Invoke-RestMethod -Method Post -Uri 'https://apoiotgfiemg.vercel.app/api/admin' -ContentType 'application/json' -Body $body
```

**Importante:**
- Um celular por fila, pra não contar dobrado
- O dia operacional vira sozinho à meia-noite (horário de Brasília)
- No painel tem exportação CSV e JSON se precisar de relatório
- Qualquer coisa me chama.

---

## Tomazeli envia pros atiradores

> **Link:** https://apoiotgfiemg.vercel.app
>
> **Como usar:**
> 1. Abra o link no celular
> 2. Escolha seu nome e o portão em que vai ficar
> 3. Use +1 ENTRADA ou +1 SAÍDA conforme o movimento
> 4. Registre cada pessoa individualmente com +1
> 5. Se marcar errado, toque em Desfazer imediatamente
> 6. Se a internet cair, continue contando normalmente — os registros sincronizam sozinhos quando voltar
> 7. Ao trocar de posto, use "Trocar posto"
>
> **Atenção:** nunca conte a mesma fila em dois celulares ao mesmo tempo.
