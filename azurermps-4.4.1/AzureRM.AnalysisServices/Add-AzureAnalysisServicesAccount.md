---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
ms.openlocfilehash: 8b5133e62139fca02dc59f84e5fb714d2a35e675
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611014"
---
# Add-AzureAnalysisServicesAccount

## Sinopse
Adiciona uma conta autenticada para usar nas solicitações do cmdlet do servidor do Azure Analysis Services.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### UserParameterSetName (padrão)
```
Add-AzureAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithPasswordParameterSetName
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential>
 [-ServicePrincipal] -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithCertificateParameterSetName
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Add-AzureAnalysisServicesAccount é usado para fazer logon em uma instância do servidor do Azure Analysis Services

## EXEMPLOS

### Exemplo 1
```
PS C:\>Add-AzureAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

Este exemplo adicionará a conta especificada pela variável $UserCredential ao ambiente do westcentralus.asazure.windows.net Analysis Services.

### Exemplo 2
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

O primeiro comando obtém as credenciais da entidade de serviço do aplicativo e, em seguida, as armazena na variável $ApplicationCredential.
O segundo comando adiciona a conta de entidade de serviço do aplicativo especificada pela variável $ApplicationCredential e Tenantid ao ambiente do westcentralus.asazure.windows.net Analysis Services.

### Exemplo 3
```
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

Este exemplo adicionará a conta da entidade de serviço do aplicativo especificada pela ApplicationId, Tenantid e CertificateThumbprint ao ambiente do westcentralus.asazure.windows.net Analysis Services.

## OS

### -ApplicationId
A ID do aplicativo.

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
Hash do certificado (impressão digital)

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Credenciais de logon

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RolloutEnvironment
Nome do ambiente do Azure Analysis Services no qual fazer logon. Considerando o nome completo do servidor por exemplo, asazure://westcentralus.asazure.windows.net/testserver, o valor correto para essa variável será westcentralus.asazure.windows.net

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipal
Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenantid
Nome ou ID do locatário

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

## EXIBE

### Microsoft. Azure. Commands. AnalysisServices. Dataplan. AsAzureProfile

## INFORMA
Alias: Login-AzureAsAccount

## LINKS RELACIONADOS

