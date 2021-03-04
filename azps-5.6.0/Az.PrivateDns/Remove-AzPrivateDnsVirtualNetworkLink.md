---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887080"
---
# Remove-AzPrivateDnsVirtualNetworkLink

## SYNOPSIS
Remove um link de rede virtual de um grupo de recursos.

## SINTAXE

### Campos (Padrão)
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** exclui permanentemente um link DNS de um grupo de recursos especificado.
Você pode passar um **objeto PSPrivateDnsVirtualNetworkLink** usando o parâmetro *Link* ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros *Name* *ZoneName* e *ResourceGroupName.*
Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.
Ao especificar o link usando um objeto **PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro *Link),* o link não será excluído se tiver sido alterado no DNS privado do Azure desde que o objeto **PSPrivateDnsVirtualNetworkLink** local foi recuperado. Isso fornece proteção para alterações de zona simultâneas. Isso pode ser suprimido usando o parâmetro *Overwrite,* que exclui a zona independentemente de alterações simultâneas.

## EXEMPLOS

### Exemplo 1: Remover um link
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

Este comando remove o link chamado mylink vinculado ao myzone.com de zona do grupo de recursos chamado MyResourceGroup.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -InputObject
O objeto de link de rede virtual a ser removido.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Especifica o nome do link a ser excluído.
Você também deve especificar o *parâmetro ResourceGroupName* e *ZoneName.*
Como alternativa, você pode especificar o link usando o *parâmetro Link.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Ao especificar a zona usando um **objeto PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro *Link),* a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **PSPrivateDnsVirtualNetworkLink** local foi recuperado.
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *Overwrite,* que exclui a zona independentemente de alterações simultâneas.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Usado para passar o resultado (booleano) da operação excluir link de rede virtual mais abaixo do pipeline.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém o link a ser removido.
Você também deve especificar o parâmetro *ZoneName* e *Name.*
Como alternativa, você pode especificar a zona DNS usando um **objeto PSPrivateDnsVirtualNetworkLink,** passado pelo pipeline ou pelo *parâmetro Link.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Especifica a ARM de recurso do link.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneName
Especifica o nome da zona DNS privada à que o link está associado.
Você também deve especificar o *parâmetro ResourceGroupName* e *Name.*
Como alternativa, você pode especificar o link usando o *parâmetro Link.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink

### System.String

## SAÍDAS

### System.Boolean

## NOTES

## LINKS RELACIONADOS

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[New-AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
