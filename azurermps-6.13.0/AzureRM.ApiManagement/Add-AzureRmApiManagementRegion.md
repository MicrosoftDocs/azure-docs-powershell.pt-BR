---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ea4b734eba1ed1a37a72e756c32acc3d6ad2a32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431479"
---
# Add-AzureRmApiManagementRegion

## Sinopse
Adiciona novas regiões de implantação a uma instância de PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmApiManagementRegion** adiciona uma nova instância do tipo **PsApiManagementRegion** à coleção de **AdditionalRegions** da instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Esse cmdlet não implanta algo sozinha, mas atualiza a instância do **PsApiManagement** na memória.
Para atualizar uma implantação de um gerenciamento de API, passe a instância **PsApiManagement** modificada para Update-AzureRmApiManagementDeployment.

## EXEMPLOS

### Exemplo 1: adicionar novas regiões de implantação a uma instância do PsApiManagement
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Esse comando adiciona duas unidades de SKU Premium e a região chamada leste EUA à instância **PsApiManagement** .

### Exemplo 2: adicionar novas regiões de implantação a uma instância do PsApiManagement e atualizar a implantação
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

Esse comando obtém um objeto **PsApiManagement** , adiciona duas unidades de SKU Premium para a região chamada leste EUA e atualiza a implantação.

## OS

### -ApiManagement
Especifica a instância **PsApiManagement** para a qual esse cmdlet adiciona mais regiões de implantação.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Capacidade
Especifica a capacidade de SKU da região de implantação.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Local
Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.
Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Especifica a camada da região de implantação.
Os valores válidos são: 
- Event
- Oficial
- Gratifica

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Especifica uma configuração de rede virtual.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
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

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement
Parâmetros: ApiManagement (ByValue)

## EXIBE

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## INFORMA
* O cmdlet grava a instância do **PsApiManagement** atualizado em pipeline.

## LINKS RELACIONADOS

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)


