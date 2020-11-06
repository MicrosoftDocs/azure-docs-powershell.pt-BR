---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432814"
---
# Set-AzureRmApiManagementApiRevision

## Sinopse
Modifica uma revisão de API

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ExpandedParameter (padrão)
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmApiManagementApiRevision** modifica uma revisão da API de gerenciamento de API do Azure.

## EXEMPLOS

### Exemplo 1 modificar uma revisão de API
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

O cmdlet atualiza a `2` revisão da API `echo-api` com uma nova descrição, protocolo e caminho.

## OS

### -ApiId
Identificador de API existente.
Esse parâmetro é obrigatório.

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApiRevision
Identificador da revisão de API existente. Esse parâmetro é obrigatório.

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuthorizationScope
Escopo de operações OAuth.
Este parâmetro é opcional.
O valor padrão é $null.

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

### -AuthorizationServerId
Identificador do servidor de autorização OAuth.
Este parâmetro é opcional.
O valor padrão é $null.
Deve ser especificado se AuthorizationScope for especificado.

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

### -Contexto
Instância do PsApiManagementContext.
Esse parâmetro é obrigatório.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
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

### -Descrição
Descrição da API Web.
Este parâmetro é opcional.

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

### -InputObject
Instância do PsApiManagementApi. Esse parâmetro é obrigatório.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome da API da Web.
Nome público da API como seria exibido nos portais de desenvolvedor e de administração.
Esse parâmetro é obrigatório.

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

### -PassThru
Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement... Model. PsApiManagementApi que representa a API Set.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminho
Caminho de API Web.
Última parte da URL pública da API.
Esta URL será usada por consumidores de API para enviar solicitações ao serviço Web.
Deve ter de 1 a 400 caracteres de comprimento.
Este parâmetro é opcional.
O valor padrão é $null.

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

### -Protocolos
Protocolos de API Web (http, HTTPS).
Protocolos em que a API é disponibilizada.
Esse parâmetro é obrigatório.
O valor padrão é $null.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceUrl
Uma URL do serviço Web que expõe a API.
Essa URL será usada apenas pelo gerenciamento de APIs do Azure e não será publicada.
Deve ter de 1 a 2000 caracteres de comprimento.
Esse parâmetro é obrigatório.

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

### -SubscriptionKeyHeaderName
Nome do cabeçalho da chave de assinatura.
Este parâmetro é opcional.
O valor padrão é $null.

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

### -SubscriptionKeyQueryParamName
Nome do parâmetro da cadeia de consulta da chave de assinatura.
Este parâmetro é opcional.
O valor padrão é $null.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext

### Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi
Parâmetros: inputobject (ByValue)

### Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []

### System. Management. Automation. SwitchParameter

## EXIBE

### Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmApiManagementApiRevision](./Get-AzureRmApiManagementApiRevision.md)

[New-AzureRmApiManagementApiRevision](./New-AzureRmApiManagementApiRevision.md)

[Remove-AzureRmApiManagementApiRevision](./Remove-AzureRmApiManagementApiRevision.md)
