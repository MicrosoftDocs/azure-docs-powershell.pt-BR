---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 52e5dce154b6798a0bddb0416235d371d6c85910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430789"
---
# Remove-AzureRmWebAppSSLBinding

## Sinopse
Remove uma associação SSL de um certificado carregado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Eles
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmWebAppSSLBinding** remove uma associação de Secure Sockets Layer (SSL) de um aplicativo Web do Azure.
Associações SSL são usadas para associar um aplicativo Web a um certificado.

## EXEMPLOS

### Exemplo 1: remover uma associação SSL para um aplicativo Web
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Esse comando Remove a associação SSL do aplicativo Web ContosoWebApp.
Como o parâmetro *DeleteCertificate* não está incluído, o certificado será excluído se não tiver mais associações SSL.

### Exemplo 2: remover uma associação SSL sem remover o certificado
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Semelhante ao exemplo 1, esse comando também remove a associação SSL do aplicativo Web ContosoWebApp.
Nesse caso, no entanto, o parâmetro *DeleteCertificate* está incluído, e o valor do parâmetro é definido como $false.
Isso significa que o certificado não será excluído independentemente de ter ou não associações SSL.

### Exemplo 3: usar uma referência de objeto para remover uma associação SSL
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

Este exemplo usa uma referência de objeto para o site do Web App para remover a associação SSL para um aplicativo Web.
O primeiro comando usa o cmdlet Get-AzureRmWebApp para criar uma referência de objeto para o aplicativo Web chamado ContosoWebApp.
Essa referência de objeto é armazenada em uma variável chamada $WebApp.
O segundo comando usa a referência de objeto e o cmdlet **Remove-AzureRmWebAppSSLBinding** para remover a associação SSL.

## OS

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

### -DeleteCertificate
Especifica a ação a ocorrer se a associação SSL que está sendo removida for a única associação usada pelo certificado.
Se *DeleteCertificate* estiver definido como $false, o certificado não será excluído quando a associação for excluída.
Se *DeleteCertificate* for definido como $true ou não for incluído no comando, o certificado será excluído juntamente com a associação SSL.
O certificado só será excluído se a associação SSL que está sendo removida for a única associação usada pelo certificado.
Se o certificado tiver mais de uma associação, o certificado não será removido, independentemente do valor do parâmetro *DeleteCertificate* .

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do aplicativo Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o certificado está atribuído.
Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Especifica o slot de implantação do aplicativo Web.
Para obter um slot de implantação, use o cmdlet Get-AzureRMWebAppSlot.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Especifica um aplicativo Web.
Para obter um aplicativo Web, use o cmdlet Get-AzureRmWebApp.
Não é possível usar o parâmetro *webapp* no mesmo comando que o parâmetro *ResourceGroupName* e/ou o *webappname*.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppname
Especifica o nome do aplicativo Web.
Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Management. WebSites. Models. site
Parâmetros: WebApp (ByValue)

## EXIBE

### System. void

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[New-AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


