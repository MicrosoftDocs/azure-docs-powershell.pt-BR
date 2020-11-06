---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427121"
---
# Get-AzureRmStorageContainer

## Sinopse
Obtém ou lista contêineres de blob de armazenamento

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### AccountName (padrão)
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Accountobject
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmStorageContainer** Obtém ou lista os contêineres de blob de armazenamento

## EXEMPLOS

### Exemplo 1: obter um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

Esse comando obtém um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.

### Exemplo 2: listar todos os contêineres de blob de armazenamento de uma conta de armazenamento
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

Esse comando lista todos os contêineres de armazenamento de blob de uma conta de armazenamento com o nome da conta de armazenamento.

### Exemplo 3: obter um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

Esse comando obtém um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do contêiner

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
Objeto da conta de armazenamento

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Nome da conta de armazenamento.

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Management. Storage. Models. PSContainer

## INFORMA

## LINKS RELACIONADOS

