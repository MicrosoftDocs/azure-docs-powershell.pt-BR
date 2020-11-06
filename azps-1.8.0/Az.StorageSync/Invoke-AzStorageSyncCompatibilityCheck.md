---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 16348feffd1f3befbb28c3e3ed73a54c2ae234ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598496"
---
# Invoke-AzStorageSyncCompatibilityCheck

## Sinopse
Verifica possíveis problemas de compatibilidade entre o sistema e a sincronização de arquivos do Azure.

## SYNTAX

### PathBased (padrão)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Invoke-AzStorageSyncCompatibilityCheck** verifica possíveis problemas de compatibilidade entre seu sistema e a sincronização de arquivos do Azure. Com um caminho local ou remoto, ele executa um conjunto de validações no namespace do sistema e do arquivo e, em seguida, retorna qualquer problema de compatibilidade encontrado.
Verificações do sistema:
- Verificações de namespace do arquivo de compatibilidade do so:
- Caracteres sem suporte
- Tamanho máximo de arquivo
- Comprimento máximo do caminho
- Tamanho máximo de arquivo
- Tamanho máximo do DataSet
- Profundidade máxima de diretório

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Esse comando verifica a compatibilidade do sistema e também de arquivos e pastas no C:\DATA.

### Exemplo 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Esse comando verifica a compatibilidade de arquivos e pastas no C:\DATA, mas não executa uma verificação de compatibilidade do sistema.

### Exemplo 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Esse comando verifica a compatibilidade do sistema e também de arquivos e pastas no C:\DATA e, em seguida, exporta os resultados como um arquivo CSV para C:\results.

## OS

### -ComputerName
O computador em que você está executando essa verificação.

```yaml
Type: String
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
Type: PSCredential
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
Type: String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNamespaceChecks
Defina esse sinalizador para ignorar validações de namespace de arquivo e executar somente validações de sistema.

```yaml
Type: SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
Defina esse sinalizador para ignorar validações do sistema e somente executar validações de namespace de arquivo.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult

## INFORMA
* Palavras-chave: Azure, AZ, ARM, Resource, Management, storagesync, filesync

## LINKS RELACIONADOS
