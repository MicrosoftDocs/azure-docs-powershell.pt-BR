---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 062df0ddadc3cc0cfb2e1f0ef9954454b08c4352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428944"
---
# Enable-AzureRmDataLakeStoreKeyVault

## Sinopse
Tenta habilitar um cofre de chaves gerenciados pelo usuário para a criptografia da conta especificada do data Lake Store.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Enable-AzureRmDataLakeStoreKeyVault** tenta habilitar um cofre de chaves gerenciados pelo usuário para a criptografia da conta especificada do data Lake Store.

## EXEMPLOS

### Exemplo 1: habilitar o cofre de chaves para a conta do ContosoADLS
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

Esse comando tenta habilitar o cofre de chave gerenciado pelo usuário para a conta do data Lake Store chamada ContosoADLS.

## OS

### -Conta
A conta do data Lake Store para habilitar o cofre de chave gerenciado pelo usuário

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -ResourceGroupName
Nome do grupo de recursos associado à conta. Se não for especificado, haverá uma tentativa de descoberta.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmDataLakeStoreAccount](./New-AzureRmDataLakeStoreAccount.md)

[Set-AzureRmDataLakeStoreAccount](./Set-AzureRmDataLakeStoreAccount.md)

