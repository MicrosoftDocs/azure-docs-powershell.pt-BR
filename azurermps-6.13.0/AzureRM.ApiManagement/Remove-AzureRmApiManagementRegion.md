---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ccd7379a07b83b3ed45eff5f8095b950868810c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609450"
---
# Remove-AzureRmApiManagementRegion

## Sinopse
Remove uma região de implantação existente da instância PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmApiManagementRegion** remove a instância do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** de uma coleção de **AdditionalRegions** da fornecida a instância do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Esse cmdlet não modifica a implantação sozinha, mas atualiza a instância do **PsApiManagement** na memória.
Para atualizar uma implantação de um gerenciamento de API, passe a **PsApiManagementInstance** modificada para **Update-AzureRmApiManagement**.

## EXEMPLOS

### Exemplo 1: remover uma região de uma instância do PsApiManagement
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Esse comando Remove a região chamada leste US da instância **PsApiManagement** .

### Exemplo 2: remover uma região de uma instância do PsApiManagement usando uma série de comandos
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

Esse primeiro comando obtém uma instância de **PsApiManagement** do grupo de recursos chamado contoso chamado ContosoApi.
Em seguida, o comando final remove a região chamada leste dos EUA dessa instância e atualiza a implantação.

## OS

### -ApiManagement
Especifica a instância **PsApiManagement** para a qual esse cmdlet Remove a região de implantação adicional.

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

### -DefaultProfile

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
Especifica o local da região que este cmdlet Remove.
Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.
Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement
Parâmetros: ApiManagement (ByValue)

### System. String

## EXIBE

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)


