---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431263"
---
# Invoke-AzureRmStorageSyncCompatibilityCheck

## Sinopse
Verifica possíveis problemas de compatibilidade entre o sistema e a sincronização de arquivos do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### PathBased (padrão)
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Invoke-AzureRmStorageSyncCompatibilityCheck** verifica possíveis problemas de compatibilidade entre seu sistema e a sincronização de arquivos do Azure. Com um caminho local ou remoto, ele executa um conjunto de validações no namespace do sistema e do arquivo e, em seguida, retorna qualquer problema de compatibilidade encontrado.
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
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

Esse comando verifica a compatibilidade do sistema e também de arquivos e pastas no C:\DATA.

### Exemplo 2
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Esse comando verifica a compatibilidade de arquivos e pastas no C:\DATA, mas não executa uma verificação de compatibilidade do sistema.

### Exemplo 3
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

Esse comando verifica a compatibilidade do sistema e também de arquivos e pastas no C:\DATA e, em seguida, exporta os resultados como um arquivo CSV para C:\results.

## OS

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

### -Quiet
Suprime o relatório de saída de gravação no console.

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

### -SkipNamespaceChecks
Defina esse sinalizador para ignorar validações de namespace de arquivo e executar somente validações de sistema.

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
Defina esse sinalizador para ignorar validações do sistema e somente executar validações de namespace de arquivo.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult

## INFORMA
* Palavras-chave: Azure, azurerm, ARM, Resource, Management, storagesync, filesync

## LINKS RELACIONADOS
