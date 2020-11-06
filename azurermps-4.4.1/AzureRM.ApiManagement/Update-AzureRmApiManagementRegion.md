---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427009"
---
# Update-AzureRmApiManagementRegion

## Sinopse
Atualiza a região de implantação existente na instância PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzureRmApiManagementRegion** atualiza uma instância existente do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** em uma coleção de objetos **AdditionalRegions** de uma instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Esse cmdlet não implanta nada, mas atualiza uma instância de **PsApiManagement** na memória.
Para atualizar uma implantação de um gerenciamento de API, use o **PsApiManagementInstance** modificado para o cmdlet Update-AzureRmApiManagementDeployment.

## EXEMPLOS

## OS

### -ApiManagement
Especifica a instância **PsApiManagement** para atualizar uma região de implantação existente no.

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
Especifica o novo valor de capacidade de SKU para a região de implantação.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica o local da região de implantação a ser atualizada.

Os valores válidos são:

- Centro Norte dos EUA
- Centro-Sul dos EUA
- Centro dos EUA
- Oeste da Europa
- Norte da Europa
- Oeste dos EUA
- Leste dos EUA
- Leste dos EUA 2
- Japão oriental
- Oeste do Japão
- Sul do Brasil
- Sudeste Asiático
- Leste da Ásia
- Leste da Austrália
- Sudeste da Austrália

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Especifica o novo valor de camada para a região de implantação.

Os valores válidos são:

- Event
- Oficial
- Gratifica

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Especifica uma configuração de rede virtual para a região de implantação.
Passar $null removerá a configuração de rede virtual para a região.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PsApiManagement
O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)
