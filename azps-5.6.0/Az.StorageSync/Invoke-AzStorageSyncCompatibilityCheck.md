---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891928"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
Verifica se há possíveis problemas de compatibilidade entre seu sistema e a Sincronização de Arquivos do Azure.

## SINTAXE

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

## DESCRIPTION
O cmdlet **Invoke-AzStorageSyncCompatibilityCheck** verifica se há possíveis problemas de compatibilidade entre seu sistema e a Sincronização de Arquivos do Azure. Dado um caminho local ou remoto, ele executa um conjunto de validações no namespace do sistema e do arquivo e retorna todos os problemas de compatibilidade que encontrar.
Verificações do sistema:
- Compatibilidade do sistema operacional Namespace de arquivo verifica:
- Caracteres sem suporte
- Tamanho máximo do arquivo
- Comprimento máximo do caminho
- Comprimento máximo do arquivo
- Tamanho máximo do conjuntos de dados
- Profundidade máxima do diretório

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Este comando verifica a compatibilidade do sistema e também de arquivos e pastas em C:\DATA.

### Exemplo 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Este comando verifica a compatibilidade de arquivos e pastas em C:\DATA, mas não executa uma verificação de compatibilidade do sistema.

### Exemplo 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Este comando verifica a compatibilidade do sistema e também de arquivos e pastas em C:\DATA e exporta os resultados como um arquivo CSV para C:\results.

## PARÂMETROS

### -ComputerName
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

### -Credential
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

### -Path
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
De definir esse sinalizador para ignorar validações de namespace de arquivo e executar somente validações do sistema.

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
De definir esse sinalizador para ignorar validações do sistema e executar apenas validações de namespace de arquivo.

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

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## NOTES
* Palavras-chave: azure, Az, arm, resource, management, storagesync, filesync

## LINKS RELACIONADOS
