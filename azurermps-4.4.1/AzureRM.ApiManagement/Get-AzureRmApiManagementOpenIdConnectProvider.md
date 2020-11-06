---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427043"
---
# Get-AzureRmApiManagementOpenIdConnectProvider

## Sinopse
Obtém provedores do OpenID Connect.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Obter todos os provedores do OpenID Connect (padrão)
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Obter ID do provedor do OpenID Connect
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Localizar pelo nome amigável do provedor de conexão OpenID
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApiManagementOpenIdConnectProvider** Obtém provedores de conexão OpenID no gerenciamento de API do Azure.

## EXEMPLOS

### Exemplo 1: obter todos os provedores
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

Este comando obtém todos os provedores do OpenID Connect para o contexto especificado.

### Exemplo 2: obter um provedor usando uma ID
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

Esse comando obtém o provedor com a ID OICProvicer01.

### Exemplo 3: obter um provedor usando um nome
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

Esse comando obtém o provedor chamado provedor de conexão de OpenID do contoso.

## OS

### -Contexto
Especifica um objeto **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica um nome amigável de um provedor.
Se você especificar um nome, esse cmdlet obterá esse provedor.

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OpenIdConnectProviderId
Especifica uma ID do provedor que este cmdlet Remove.
Se você especificar uma ID, esse cmdlet obterá esse provedor.

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
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

## EXIBE

### IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider>

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmApiManagementOpenIdConnectProvider](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[Remove-AzureRmApiManagementOpenIdConnectProvider](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[Set-AzureRmApiManagementOpenIdConnectProvider](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


