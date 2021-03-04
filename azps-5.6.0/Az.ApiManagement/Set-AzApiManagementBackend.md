---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: a6428498f9d839be0fd99104ec759b0eb08912dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893246"
---
# Set-AzApiManagementBackend

## SYNOPSIS
Atualiza um Back-end.

## SINTAXE

### ContextParameterSet (Padrão)
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Atualiza um back-end existente no Gerenciamento de Api.

## EXEMPLOS

### Exemplo 1: atualiza a Descrição do Backend 123
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

### Exemplo 2

Atualiza um Back-end. (gerado automaticamente)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementBackend -BackendId 123 -Context <PsApiManagementContext> -Credential <PsApiManagementBackendCredential> -Protocol http -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso -Url 'https://contoso.com/awesomeapi'
```

## PARÂMETROS

### -BackendId
Identificador de novo back-end.
Esse parâmetro é necessário.

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Instância de PsApiManagementContext.
Esse parâmetro é necessário.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Credential
Detalhes da credencial que devem ser usados ao falar com o Backend.
Esse parâmetro é opcional.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -Description
Descrição de back-end.
Esse parâmetro é opcional.

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
Instância de PsApiManagementBackend. Esse parâmetro é necessário.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Indica que esse cmdlet retorna  **o PsApiManagementBackend** que este cmdlet modifica.

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

### -Protocol
Protocolo de Comunicação back-end (http ou soap).
Esse parâmetro é opcional

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Proxy
Detalhes do Servidor Proxy a serem usados durante o envio da solicitação para o Backend.
Esse parâmetro é opcional.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Uri de gerenciamento do Recurso no Sistema Externo.
Esse parâmetro é opcional.
Essa url pode ser a ID de Recurso arm de Aplicativos Lógicos, Aplicativos de Função ou Aplicativos de Api.

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

### -ServiceFabricCluster
Detalhes do Back-end do Cluster de Malha de Serviço. Esse parâmetro é opcional.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipCertificateChainValidation
Se ignorar a validação da cadeia de certificados ao falar com o Backend.
Esse parâmetro é opcional.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipCertificateNameValidation
Se deve ignorar Validação de Nome de Certificado ao falar com o Backend.
Esse parâmetro é opcional.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Title
Título back-end.
Esse parâmetro é opcional.

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

### -Url
Url do tempo de execução para o Backend.
Esse parâmetro é opcional.

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

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric

### System.Management.Automation.SwitchParameter

## SAÍDAS

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend

## NOTES

## LINKS RELACIONADOS

[Get-AzApiManagementBackend](./Get-AzApiManagementBackend.md)

[New-AzApiManagementBackend](./New-AzApiManagementBackend.md)

[New-AzApiManagementBackendCredential](./New-AzApiManagementBackendCredential.md)

[New-AzApiManagementBackendProxy](./New-AzApiManagementBackendProxy.md)

[Remove-AzApiManagementBackend](./Remove-AzApiManagementBackend.md)
