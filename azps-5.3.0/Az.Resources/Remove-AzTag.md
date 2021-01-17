---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429471"
---
# Remove-AzTag

## Sinopse
Exclui valores ou marcas do Azure predefinidas | Exclui todo o conjunto de marcas em um recurso ou assinatura.

## SYNTAX

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

## DESCRITIVO

**RemovePredefinedTagSet**: o cmdlet **Remove-AzTag** exclui as marcas e os valores predefinidos do Azure de sua assinatura.
Para excluir valores específicos de uma marca predefinida, use o parâmetro *Value* .
Por padrão, **Remove-AzTag** exclui a marca especificada e todos os seus valores. Não é possível excluir uma marca ou um valor que seja aplicado no momento a um recurso ou grupo de recursos.
Antes de usar **Remove-AzTag**, use o parâmetro *Tag* do cmdlet Set-AzResourceGroup para excluir a marca ou os valores do recurso ou do grupo de recursos.
O módulo de marcas do Azure que **Remove-AzTag** faz parte do pode ajudá-lo a gerenciar suas marcas predefinidas do Azure.
Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.
Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.

**RemoveByResourceIdParameterSet**: o cmdlet **Remove-AzTag** com uma **ResourceId** exclui todo o conjunto de marcas em um recurso ou assinatura.

## EXEMPLOS

### Exemplo 1: excluir uma marca predefinida
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Esse comando exclui a marca predefinida chamada Department e todos os seus valores.
Se a marca tiver sido aplicada a recursos ou grupos de recursos, o comando falhará.

### Exemplo 2: excluir um valor de uma marca predefinida
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

Esse comando exclui o valor HumanResources da marca de departamento predefinida.
Ele não exclui a marca.
Se o valor tiver sido aplicado a recursos ou grupos de recursos, o comando falhará.

### Exemplo 3: exclui todo o conjunto de marcas em uma assinatura

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Esse comando exclui todo o conjunto de marcas na assinatura com {subId}. Ele não retornará o objeto excluído se não passar "-PassThru".

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

Esse comando exclui todo o conjunto de marcas no recurso com {ResourceId}. Ele retorna o oject excluído ao passar "-PassThru".

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

### -Nome
Especifica o nome da marca predefinida a ser removida.
Por padrão, **Remove-AzTag** remove a marca especificada e todos os seus valores.
Para excluir os valores selecionados, mas não excluir a marca, use o parâmetro *Value* .

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

### -Valor
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
O identificador de recurso para a entidade marcada. Um recurso, um grupo de recursos ou uma assinatura pode estar marcado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### System. String []

### System. Management. Automation. SwitchParameter

## EXIBE

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## INFORMA

## LINKS RELACIONADOS

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)