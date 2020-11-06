---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427048"
---
# Get-AzureRmApiManagement

## Sinopse
Obtém uma lista ou uma descrição de serviço de gerenciamento de API específica.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Todos na assinatura (padrão)
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Tudo no grupo de recursos
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Serviço de gerenciamento de API específico
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApiManagement** Obtém uma lista de todos os serviços de gerenciamento de API sob assinatura ou grupo de recursos especificado ou um gerenciamento de API específico.

## EXEMPLOS

### Exemplo 1: obter todos os serviços de gerenciamento de API
```
PS C:\>Get-AzureRmApiManagement
```

Esse comando obtém todos os serviços de gerenciamento de API em uma assinatura.

### Exemplo 2: obter todos os serviços de gerenciamento de API por um nome específico
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

Esse comando obtém todo o serviço de gerenciamento de API por nome.

## OS

### -Nome
Especifica o nome do serviço de gerenciamento de API.

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos em que esse cmdlet obtém o serviço de gerenciamento de API.

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
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

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement]

## INFORMA

## LINKS RELACIONADOS

[Backup-AzureRmApiManagement](./Backup-AzureRmApiManagement.md)

[New-AzureRmApiManagement](./New-AzureRmApiManagement.md)

[Remove-AzureRmApiManagement](./Remove-AzureRmApiManagement.md)

[Restore-AzureRmApiManagement](./Restore-AzureRmApiManagement.md)


