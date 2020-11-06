---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b9154b239e8d4ae2857cba18d3f7dcf9510a62b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427240"
---
# Set-AzureRmDataLakeStoreAccount

## Sinopse
Modifica uma conta do data Lake Store.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmDataLakeStoreAccount** modifica uma conta do data Lake Store.

## EXEMPLOS

### Exemplo 1: adicionar uma marca a uma conta
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

Esse comando adiciona a marca especificada à conta data Lake Store chamada ContosoADL.

## OS

### -AllowAzureIpState
Opcionalmente, permitir/bloquear IPs de origem do Azure por meio do firewall.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultGroup
Especifica a ID de um grupo de diretórios do AzureActive.
Este grupo é o grupo padrão para arquivos e pastas que você criar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Firewallstate
Opcionalmente, habilite ou desabilite as regras de firewall existentes.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Keyversion
Se o tipo de criptografia for atribuído pelo usuário, o usuário poderá girar a respectiva versão da chave com esse parâmetro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome de uma conta do repositório data Lake.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser modificada.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Especifica marcas como pares de valor chave.
Você pode usar marcas para identificar uma conta do data Lake Store de outros recursos do Azure.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier
A camada de compromisso desejada para esta conta usar.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TrustedIdProviderState
Opcionalmente, habilite ou desabilite os provedores de ID confiáveis existentes.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. Collections. Hashtable

### System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. Firewallstate, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. Tiertype, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## EXIBE

### Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmDataLakeStoreAccount](./Get-AzureRmDataLakeStoreAccount.md)

[New-AzureRmDataLakeStoreAccount](./New-AzureRmDataLakeStoreAccount.md)

[Remove-AzureRmDataLakeStoreAccount](./Remove-AzureRmDataLakeStoreAccount.md)

[Test-AzureRmDataLakeStoreAccount](./Test-AzureRmDataLakeStoreAccount.md)


