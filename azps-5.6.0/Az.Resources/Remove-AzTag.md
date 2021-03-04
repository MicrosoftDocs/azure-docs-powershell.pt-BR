---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 201e341ce05b22597f05601d7d269d2eb27c2358
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888814"
---
# Remove-AzTag

## SYNOPSIS
Exclui marcas ou valores predefinidos do Azure | Exclui todo o conjunto de marcas em um recurso ou assinatura.

## SINTAXE

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## DESCRIPTION

**RemovePredefinedTagSet**: o cmdlet **Remove-AzTag** exclui marcas e valores predefinidos do Azure da sua assinatura.
Para excluir valores específicos de uma marca predefinida, use o *parâmetro Value.*
Por padrão, **Remove-AzTag** exclui a marca especificada e todos os seus valores. Não é possível excluir uma marca ou um valor que está atualmente aplicado a um grupo de recursos ou recursos.
Antes de **usar Remove-AzTag**, use o parâmetro *Tag* do cmdlet Set-AzResourceGroup para excluir a marca ou os valores do grupo de recursos ou recursos.
O módulo Marcas do Azure do que **Remove-AzTag** faz parte pode ajudá-lo a gerenciar suas marcas predefinidas do Azure.
Uma marca do Azure é um par de valores de nome que você pode usar para categorizar seus recursos e grupos de recursos do Azure, como departamento ou centro de custo, ou para acompanhar observações ou comentários sobre os recursos e grupos.
Você pode definir e aplicar marcas em uma única etapa, mas marcas predefinida permitem estabelecer nomes e valores padrão, consistentes e previsíveis para as marcas em sua assinatura.

**RemoveByResourceIdParameterSet**: o cmdlet **Remove-AzTag** com **um ResourceId** exclui todo o conjunto de marcas em um recurso ou assinatura.

## EXEMPLOS

### Exemplo 1: Excluir uma marca predefinida
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Este comando exclui a marca predefinida chamada Department e todos os seus valores.
Se a marca tiver sido aplicada a quaisquer recursos ou grupos de recursos, o comando falhará.

### Exemplo 2: Excluir um valor de uma marca predefinida
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Este comando exclui o valor HumanResources da marca Department predefinida.
Ele não exclui a marca.
Se o valor tiver sido aplicado a quaisquer recursos ou grupos de recursos, o comando falhará.

### Exemplo 3: exclui todo o conjunto de marcas em uma assinatura

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Este comando exclui todo o conjunto de marcas na assinatura com {subId}. Ele não retornará o objeto excluído se não passar "-PassThru".

### Exemplo 4: exclui todo o conjunto de marcas em um recurso

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Este comando exclui todo o conjunto de marcas no recurso com {resourceId}. Ele retorna o oject excluído ao passar "-PassThru".

## PARÂMETROS

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

### -Name
Especifica o Nome da marca predefinida a ser removido.
Por padrão, **Remove-AzTag** remove a marca especificada e todos os seus valores.
Para excluir valores selecionados, mas não excluir a marca, use o *parâmetro Value.*

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Exclui os valores especificados da marca predefinida, mas não exclui a marca.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
O identificador de recurso da entidade marcada. Um recurso, um grupo de recursos ou uma assinatura podem ser marcados.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Retorna um objeto que representa a marca excluída ou a marca resultante com valor excluído.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.String[]

### System.Management.Automation.SwitchParameter

## SAÍDAS

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTES

## LINKS RELACIONADOS

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)