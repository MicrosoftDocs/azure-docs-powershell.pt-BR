---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 7093b51ffee3f0ad635da7a6c0b63d26e93e5f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428637"
---
# Set-AzureRmApiManagementHostnames

## Sinopse
Define uma configuração de nome de host personalizada para um proxy ou um portal do serviço de gerenciamento de API.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SetSpecificService (padrão)
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetFromPsApiManagementInstance
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmApiManagementHostnames** aplica uma configuração de nome de host personalizada a um proxy ou portal do serviço de gerenciamento de API.

## EXEMPLOS

### Exemplo 1: definir a configuração do nome do host personalizado para um proxy e um portal
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

Este comando define a configuração do nome do host personalizado para o proxy e o Portal.

### Exemplo 2: configurar um nome de host personalizado para um proxy e um portal
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

Este exemplo configura um nome de host personalizado para proxy e Portal.
Você precisa importar certificados correspondentes e, em seguida, aplicar os nomes de hosts personalizados.

## OS

### -ApiManagement
Especifica a instância **PsApiManagement** para a qual esse cmdlet obtém os parâmetros *PortalHostnameConfiguration* e *ProxyHostnameConfiguration* .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Nome
Especifica o nome da instância de gerenciamento de API.

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Retorna um objeto que representa o item com o qual você está trabalhando.
Por padrão, esse cmdlet não gera nenhuma saída.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PortalHostnameConfiguration
Especifica a configuração do nome do host do portal personalizado.
Passar $null para o cmdlet define o nome do host padrão.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProxyHostnameConfiguration
Especifica a configuração do nome do host de proxy personalizado.
Passar $null define o nome do host padrão.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos sob o qual existe a instância de gerenciamento de API.

```yaml
Type: System.String
Parameter Sets: SetSpecificService
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

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration

## EXIBE

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## INFORMA

## LINKS RELACIONADOS

[Import-AzureRmApiManagementHostnameCertificate](./Import-AzureRmApiManagementHostnameCertificate.md)

[New-AzureRmApiManagementHostnameConfiguration](./New-AzureRmApiManagementHostnameConfiguration.md)


