---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118845"
---
# Remove-AzWebAppSSLBinding

## Sinopse
Remove uma encadernação SSL de um certificado carregado.

## Sintaxe

### S1
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

## Descrição
O cmdlet **Remove-AzWebAppSSLBinding** remove uma encadernação SSL (Secure Sockets Layer) de um Azure Web App.
As associações SSL são usadas para associar um Web App a um certificado.

## Exemplos

### Exemplo 1: Remover uma associação SSL para um aplicativo Web
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Esse comando remove a associação SSL do aplicativo Web ContosoWebApp.
Como o *parâmetro DeleteCertificate* não está incluído, o certificado será excluído se ele não tiver mais nenhuma associação SSL.

### Exemplo 2: Remover uma associação SSL sem remover o certificado
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Semelhante ao Exemplo 1, esse comando também remove a associação SSL do Web App ContosoWebApp.
Nesse caso, no entanto, o parâmetro *DeleteCertificate* é incluído e o valor do parâmetro é definido como $False.
Isso significa que o certificado não será excluído independentemente de ter alguma vinculação SSL ou não.

### Exemplo 3: Usar uma referência de objeto para remover uma associação SSL
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

Este exemplo usa uma referência de objeto ao site do Web App para remover a associação SSL de um Web App.
O primeiro comando usa o cmdlet Get-AzWebApp para criar uma referência de objeto ao Web App chamada ContosoWebApp.
Essa referência de objeto é armazenada em uma variável chamada $WebApp.
O segundo comando usa a referência de objeto e o cmdlet **Remove-AzWebAppSSLBinding** para remover a associação SSL.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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
Especifica a ação a ser realizada se a encadernação SSL que está sendo removida for a única associação usada pelo certificado.
Se *DeleteCertificate* estiver definido como $False, o certificado não será excluído quando a associação for excluída.
Se *DeleteCertificate* estiver definido como $True ou não estiver incluído no comando, o certificado será excluído juntamente com a associação SSL.
O certificado só será excluído se a associação SSL for removida for a única vinculação usada pelo certificado.
Se o certificado tiver mais de uma vinculação, o certificado não será removido independentemente do valor do parâmetro *DeleteCertificate.*

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

### -Forçar
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
Especifica o nome do Web App.

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
Especifica o nome do grupo de recursos ao que o certificado foi atribuído.
Você não pode usar *o parâmetro ResourceGroupName* e o parâmetro *WebApp* no mesmo comando.

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
Especifica o slot de implantação do Web App.
Para obter um slot de implantação, use Get-AzWebAppSlot cmdlet.

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
Especifica um Web App.
Para obter um Web App, use o Get-AzWebApp cmdlet.
Você não pode usar o parâmetro *WebApp* no mesmo comando que o parâmetro *ResourceGroupName* e/ou *WebAppName.*

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

### -WebAppName
Especifica o nome do Web App.
Você não pode usar o parâmetro *WebAppName* e o parâmetro *WebApp* no mesmo comando.

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

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## Saídas

### System.Void

## Notas

## LINKS RELACIONADOS

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


