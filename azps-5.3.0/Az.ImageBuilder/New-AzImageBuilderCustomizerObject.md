---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426834"
---
# New-AzImageBuilderCustomizerObject

## Sinopse
Descreve uma unidade de personalização de imagens

## SYNTAX

### ShellCustomizer (padrão)
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### Filecustomizador
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### PowerShellCustomizer
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### RestartCustomizer
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### WindowsUpdateCustomizer
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## DESCRITIVO
Descreve uma unidade de personalização de imagens

## EXEMPLOS

### Exemplo 1: criar um personalizador de atualização do Windows
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

Esse comando cria um personalizador de atualização do Windows.

### Exemplo 2: criar um personalizador de arquivos
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

Esse comando cria um personalizador de arquivos.

### Exemplo 3: criar um personalizador do PowerShell
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

Esse comando cria um personalizador do PowerShell.

### Exemplo 4: criar um personalizador de reinicialização
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

Esse comando cria um personalizador de reinício.

### Exemplo 5: criar um personalizador de Shell
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

Esse comando cria um personalizador de Shell.

## OS

### -CustomizerName
Nome amigável para fornecer contexto sobre o que essa etapa de personalização faz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destino
O caminho absoluto para um arquivo (com estruturas de diretório aninhadas já criadas) em que o arquivo (de sourceUri) será carregado na VM.

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filecustomizador
Carrega arquivos para VMs (Linux, Windows).
Corresponde ao provisionador de arquivo do Pack.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filtro
Matriz de filtros para selecionar as atualizações a serem aplicadas.
Omita ou especifique uma matriz vazia para usar o padrão (sem filtro).
Consulte o link acima para obter exemplos e descrição detalhada desse campo.

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inline
Matriz de comandos do Shell para executar.

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PowerShellCustomizer
Executa o PowerShell especificado na VM (Windows).
Corresponde ao provisionador do PowerShell do Pack.
Exatamente um de "scriptUri" ou "inline" pode ser especificado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartCheckCommand
Comando para verificar se a reinicialização foi bem-sucedida [padrão: ' '].

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartCommand
Comando para executar a reinicialização [padrão: ' shutdown/r/f/t 0/c Packer restart ']

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartCustomizer
Reinicializa uma VM e aguarda que ela volte online (Windows).
Corresponde ao provisionamento do Pack do Windows-reinício de reinicialização.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartTimeout
Reiniciar o tempo limite especificado como uma cadeia de magnitude e uma unidade, por exemplo, "5m" (5 minutos) ou "segundo" (2 horas) [padrão: "5m"].

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunElevated
Se especificado, o script do PowerShell será executado com privilégios elevados.

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptUri
URL do script do Shell a ser executada para personalização.
Pode ser um link do GitHub, URI de SAS para armazenamento do Azure, etc.

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchCriterion
Critérios para Pesquisar atualizações.
Omita ou especifique uma cadeia de caracteres vazia para usar o padrão (pesquisar tudo).
Consulte o link acima para obter exemplos e descrição detalhada desse campo.

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sha256Checksum
A soma de verificação SHA256 do script de shell fornecido no campo scriptUri.

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShellCustomizer
Executa um script de shell durante a fase de personalização (Linux).
Corresponde ao provisionador do shell do Packer.
Exatamente um de "scriptUri" ou "inline" pode ser especificado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceUri
O URI do arquivo a ser carregado para personalizar a VM.
Pode ser um link do GitHub, URI de SAS para armazenamento do Azure, etc.

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateLimit
Número máximo de atualizações a serem aplicadas de cada vez.
Omita ou especifique 0 para usar o padrão (1000).

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidExitCode
Códigos de saída válidos para o script do PowerShell.
[Padrão: 0].

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsUpdateCustomizer
Instala as atualizações do Windows.
Corresponde ao provisionador do pacote de atualizações do Windows ( https://github.com/rgl/packer-provisioner-windows-update) .

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateCustomizer

## INFORMA

ALIASES

## LINKS RELACIONADOS

