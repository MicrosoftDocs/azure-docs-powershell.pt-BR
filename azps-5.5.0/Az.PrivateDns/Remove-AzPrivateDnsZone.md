---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114992"
---
# Remove-AzPrivateDnsZone

## Sinopse
Remove uma zona DNS privada de um grupo de recursos.

## Sintaxe

### Campos (Padrão)
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Resourceid
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Remove-AzPrivateDnsZone** exclui permanentemente uma zona DNS (Sistema de Nomes de Domínio) particular de um grupo de recursos especificado.
Todos os conjuntos de registros contidos na zona também são excluídos.
Você pode passar um objeto **PrivateDnsZone** usando o parâmetro *PrivateZone* ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros *Nome* e *ResourceGroupName.*
Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.
Ao especificar a zona usando um objeto **PrivateDnsZone** (passado pelo parâmetro pipeline ou Zona), a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **Local PrivateDnsZone** foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, as operações em conjuntos de registros dentro da zona não o fazem). 
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *Substituir,* que exclui a zona independentemente das alterações simultâneas.

## Exemplos

### Exemplo 1: Remover uma zona particular
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Esse comando remove a zona chamada myzone.com do grupo de recursos chamado MyResourceGroup.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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
Especifica o nome da zona DNS privada que este cmdlet remove.
Você também deve especificar o parâmetro *ResourceGroupName.*
Como alternativa, você pode especificar a zona DNS usando o *parâmetro* Zona.

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
Ao especificar a zona usando um objeto **PrivateDnsZone** (passado pelo parâmetro pipeline ou Zona), a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **Local PrivateDnsZone** foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, as operações em conjuntos de registros dentro da zona não o fazem). 
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *Substituir,* que exclui a zona independentemente das alterações simultâneas.

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
Usado para passar o resultado (boolano) da operação, exclua a zona privada mais abaixo do pipeline.

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
Especifica o nome do grupo de recursos que contém a zona a ser removido.
Você também deve especificar o parâmetro *ZoneName.*
Como alternativa, você pode especificar a zona DNS usando um objeto **PrivateDnsZone,** passado pelo pipeline ou pelo parâmetro *Zona.*

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
ID de Recurso de Zona DNS Particular.

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

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

### System.String

## Saídas

### System.Boolean

## Notas

## LINKS RELACIONADOS

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
