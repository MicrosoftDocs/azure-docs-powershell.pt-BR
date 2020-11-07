---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
ms.openlocfilehash: 5371b5c54cfaff4b1c48dd8a8643e0cc51b1e00e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785603"
---
# Get-AzureRmStorageAccountNameAvailability

## Sinopse
Verifica a disponibilidade de um nome de conta de armazenamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmStorageAccountNameAvailability** verifica se o nome de uma conta de armazenamento do Azure é válido e está disponível para uso.

## EXEMPLOS

### Exemplo 1: verificar a disponibilidade de um nome de conta de armazenamento
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

Esse comando verifica a disponibilidade do nome ContosoStorage03.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da conta de armazenamento que este cmdlet verifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

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

### Microsoft. Azure. Management. Storage. Models. CheckNameAvailabilityResult

## INFORMA

## LINKS RELACIONADOS

[Cmdlets do Azure Storage Manager](./AzureRM.Storage.md)


