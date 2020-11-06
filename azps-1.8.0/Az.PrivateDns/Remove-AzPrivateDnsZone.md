---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d54dac2689fd751663ebf0046288c4d4ceeae928
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599767"
---
# Remove-AzPrivateDnsZone

## Sinopse
Remove uma zona DNS privada de um grupo de recursos.

## SYNTAX

### Campos (padrão)
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Identificação
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzPrivateDnsZone** exclui permanentemente uma zona de sistema de nome de domínio (DNS) privada de um grupo de recursos especificado.
Todos os conjuntos de registros contidos na zona também são excluídos.
Você pode passar um objeto **PrivateDnsZone** usando o parâmetro *PrivateZone* ou usando o operador pipeline ou, como alternativa, pode especificar o *nome* e os parâmetros de *ResourceGroupName* .
Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.
Ao especificar a zona usando um objeto **PrivateDnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não será excluída se ela tiver sido alterada no Azure DNS desde que o objeto **PrivateDnsZone** local tenha sido recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.

## EXEMPLOS

### Exemplo 1: remover uma zona privada
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Esse comando Remove a zona chamada myzone.com do grupo de recursos chamado MyResource Group.

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

### -Nome
Especifica o nome da zona DNS privada que este cmdlet Remove.
Você também deve especificar o parâmetro *ResourceGroupName* .
Você também pode especificar a zona DNS usando o parâmetro *Zone* .

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
Ao especificar a zona usando um objeto **PrivateDnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não será excluída se ela tiver sido alterada no Azure DNS desde que o objeto **PrivateDnsZone** local tenha sido recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).
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
Usado para passar o resultado (booliano) da operação excluir zona privada mais adiante no pipeline.

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

### -PrivateZone
O objeto de zona particular a ser excluído.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a zona a ser removida.
Você também deve especificar o parâmetro *zonename* .
Como alternativa, você pode especificar a zona DNS usando um objeto **PrivateDnsZone** , transmitido via o pipeline ou o parâmetro *Zone* .

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
ResourceId de zona DNS particular.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone

### System. String

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
