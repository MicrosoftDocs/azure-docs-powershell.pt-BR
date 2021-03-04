---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892908"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
Remove uma região de implantação existente da instância PsApiManagement.

## SINTAXE

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Remove-AzApiManagementRegion** remove instância do tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** de uma coleção **de AdditionalRegions** do tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.
Este cmdlet não modifica a implantação por si só, mas atualiza a instância **de PsApiManagement** na memória.
Para atualizar uma implantação de um Gerenciamento de API, passe o **PsApiManagementInstance** modificado para **Set-AzApiManagement**.

## EXEMPLOS

### Exemplo 1: Remover uma região de uma instância PsApiManagement
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Este comando remove a região chamada East US da **instância PsApiManagement.**

### Exemplo 2: Remover uma região de uma instância PsApiManagement usando uma série de comandos
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Este primeiro comando obtém uma instância **de PsApiManagement** do grupo de recursos chamado ContosoApi.
Em seguida, o comando final remove a região chamada Leste dos EUA dessa instância e atualiza a implantação.

## PARÂMETROS

### -ApiManagement
Especifica a **instância PsApiManagement** da onde esse cmdlet remove a região de implantação adicional.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Especifica o local da região que esse cmdlet remove.
Especifica o local da nova região de implantação entre a região suportada para o serviço de Gerenciamento de Api.
Para obter locais válidos, use o cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | onde {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object locais

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTES

## LINKS RELACIONADOS

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


