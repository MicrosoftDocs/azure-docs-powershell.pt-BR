---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116080"
---
# Invoke-AzStorageSyncCompatibilityCheck

## Sinopse
Verifica se há possíveis problemas de compatibilidade entre seu sistema e a Sincronização de Arquivos do Azure.

## Sintaxe

### PathBased (Padrão)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## Descrição
O cmdlet **Invoke-AzStorageSyncCompatibilityCheck** verifica possíveis problemas de compatibilidade entre seu sistema e a Sincronização de Arquivos do Azure. Dado um caminho local ou remoto, ele executa um conjunto de validações no sistema e no namespace de arquivo e retorna todos os problemas de compatibilidade encontrados.
O sistema verifica:
- O namespace de arquivo de compatibilidade do sistema operacional verifica:
- Caracteres sem suporte
- Tamanho máximo de arquivo
- Comprimento máximo do caminho
- Comprimento máximo do arquivo
- Tamanho máximo do conjuntos de dados
- Profundidade máxima do diretório

## Exemplos

### Exemplo 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Esse comando verifica a compatibilidade do sistema e também de arquivos e pastas em C:\DATA.

### Exemplo 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Esse comando verifica a compatibilidade de arquivos e pastas em C:\DATA, mas não executa uma verificação de compatibilidade do sistema.

### Exemplo 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Esse comando verifica a compatibilidade do sistema e também de arquivos e pastas em C:\DATA e exporta os resultados como um arquivo CSV para C:\resultados.

## Parâmetros

### -NomedoCompr computador
O computador em que você está executando essa verificação.

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credencial
Suas credenciais para o compartilhamento que você está validando.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caminho
O caminho UNC do compartilhamento que você está validando.

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNamespaceChecks
De definir esse sinalizador para ignorar as validações de namespace de arquivo e executar somente validações do sistema.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
De definir esse sinalizador para ignorar as validações do sistema e executar somente validações de namespace de arquivo.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## Notas
* Palavras-chave: azure, Az, arm, resource, management, storagesync, filesync

## LINKS RELACIONADOS
