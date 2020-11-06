---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426848"
---
# Get-AzureRmApiManagementSubscription

## Sinopse
Obtém assinaturas.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### GetAllSubscriptions (padrão)
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySubscriptionId
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByUserId
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByProductId
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApiManagementSubscription** Obtém uma assinatura especificada, ou todas as assinaturas, se nenhuma assinatura for especificada.

## EXEMPLOS

### Exemplo 1: obter todas as assinaturas
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

Este comando obtém todas as assinaturas.

### Exemplo 2: obter uma assinatura com uma ID especificada
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

Este comando obtém uma assinatura por ID.

### Exemplo 3: obter todas as assinaturas de um usuário
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

Este comando obtém as assinaturas de um usuário.

### Exemplo 4: obter todas as assinaturas de um produto
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

Este comando obtém todas as assinaturas do produto.

## OS

### -Contexto
Especifica um objeto **PsApiManagementContext** .

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductId
Especifica um identificador de produto.
Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador do produto.

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionId
Especifica um identificador de assinatura.
Se especificado, esse cmdlet localiza a assinatura pelo identificador.

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
Especifica um identificador de usuário.
Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador de usuário.

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription
O detalhe da assinatura no serviço de gerenciamento de API.

### IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription>
A lista de assinaturas no serviço de gerenciamento de API.

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmApiManagementSubscription](./New-AzureRmApiManagementSubscription.md)

[Remove-AzureRmApiManagementSubscription](./Remove-AzureRmApiManagementSubscription.md)

[Set-AzureRmApiManagementSubscription](./Set-AzureRmApiManagementSubscription.md)


