---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427788"
---
# Remove-AzWebAppSSLBinding

## Sinopse
Remove uma associação SSL de um certificado carregado.

## SYNTAX

### Eles
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzWebAppSSLBinding** remove uma associação de Secure Sockets Layer (SSL) de um aplicativo Web do Azure.
Associações SSL são usadas para associar um aplicativo Web a um certificado.

## EXEMPLOS

### Exemplo 1: remover uma associação SSL para um aplicativo Web
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Esse comando Remove a associação SSL do aplicativo Web ContosoWebApp.
Como o parâmetro *DeleteCertificate* não está incluído, o certificado será excluído se não tiver mais associações SSL.

### Exemplo 2: remover uma associação SSL sem remover o certificado
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Semelhante ao exemplo 1, esse comando também remove a associação SSL do aplicativo Web ContosoWebApp.
Nesse caso, no entanto, o parâmetro *DeleteCertificate* está incluído, e o valor do parâmetro é definido como $false.
Isso significa que o certificado não será excluído independentemente de ter ou não associações SSL.

### Exemplo 3: usar uma referência de objeto para remover uma associação SSL
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

Este exemplo usa uma referência de objeto para o site do Web App para remover a associação SSL para um aplicativo Web.
O primeiro comando usa o cmdlet Get-AzWebApp para criar uma referência de objeto para o aplicativo Web chamado ContosoWebApp.
Essa referência de objeto é armazenada em uma variável chamada $WebApp.
O segundo comando usa a referência de objeto e o cmdlet **Remove-AzWebAppSSLBinding** para remover a associação SSL.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Para obter um slot de implantação, use o cmdlet Get-AzWebAppSlot.

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
Para obter um aplicativo Web, use o cmdlet Get-AzWebApp.
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. webapps. Models. PSSite

## EXIBE

### System. void

## INFORMA

## LINKS RELACIONADOS

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


