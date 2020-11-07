---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941012"
---
# Remove-AzPrivateDnsVirtualNetworkLink

## Sinopse
Remove um link de rede virtual de um grupo de recursos.

## SYNTAX

### Campos (padrão)
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Identificação
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** exclui permanentemente um link DNS (sistema de nomes de domínio) privado de um grupo de recursos especificado.
Você pode passar um objeto **PSPrivateDnsVirtualNetworkLink** usando o parâmetro de *link* ou usando o operador de pipeline ou, como alternativa, pode especificar o *nome* *zonename* e os parâmetros *ResourceGroupName* .
Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.
Ao especificar o link usando um objeto **PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro do *link* ), o link não será excluído se tiver sido alterado no DNS privado do Azure desde que o objeto **PSPrivateDnsVirtualNetworkLink** local foi recuperado. Isso fornece proteção para alterações de zona simultâneas. Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.

## EXEMPLOS

### Exemplo 1: remover um link
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

Esse comando Remove o link nomeado MyLink vinculado à Zone myzone.com do grupo de recursos chamado MyResource Group.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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
O objeto de conexão de rede virtual a ser removido.

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

### -Nome
Especifica o nome do link a ser excluído.
Você também deve especificar o parâmetro *ResourceGroupName* e *zonename* .
Ou, se preferir, você pode especificar o link usando o parâmetro de *link* .

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

### -Substituir
Ao especificar a zona usando um objeto **PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro do *link* ), a zona não é excluída se foi alterada no Azure DNS desde que o objeto **PSPrivateDnsVirtualNetworkLink** local foi recuperado.
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.

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
Usado para passar o resultado (booliano) da operação excluir o link de rede virtual mais adiante no pipeline.

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
Você também deve especificar *zonename* e o parâmetro *Name* .
Como alternativa, você pode especificar a zona DNS usando um objeto **PSPrivateDnsVirtualNetworkLink** , passado pelo pipeline ou pelo parâmetro de *link* .

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
Especifica a ID do recurso ARM do link.

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

### -Zonename
Especifica o nome da zona DNS privada à qual o link está associado.
Você também deve especificar o parâmetro *ResourceGroupName* e *Name* .
Ou, se preferir, você pode especificar o link usando o parâmetro de *link* .

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

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink

### System. String

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[New-AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
