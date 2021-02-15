---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112630"
---
# New-AzTag

## Sinopse
Cria uma marca predefinida do Azure ou adiciona valores a uma marca existente | Cria ou atualiza todo o conjunto de marcas em um recurso ou assinatura.

## Sintaxe

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## Descrição

**CreatePredefinedTagSet:** o cmdlet **New-AzTag** cria uma marca predefinida do Azure com um valor predefinido opcional.
Você também pode usá-lo para adicionar valores adicionais a marcas predefinidos existentes.
Para criar uma marca predefinida, insira um nome de marca exclusivo.
Para adicionar um valor a uma marca predefinida existente, especifique o nome da marca existente e o novo valor.
Este cmdlet retorna um objeto que representa a marca nova ou modificada com seus valores e o número de recursos aos quais ele foi aplicado.
O módulo Marcas do Azure **do que o New-AzTag** faz parte pode ajudá-lo a gerenciar marcas predefinidas do Azure.
Uma marca do Azure é um par de valores de nome que você pode usar para categorizar seus recursos e grupos de recursos do Azure, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.
Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinida permitem estabelecer nomes e valores padrão, consistentes e previsíveis para as marcas em sua assinatura.
Para aplicar uma marca predefinida a um grupo de recursos ou recursos, use o parâmetro *Tag* do cmdlet New-AzTag.
Para procurar grupos de recursos com um nome ou  um nome e um valor de marca especificados, use o parâmetro Tag do cmdlet Get-AzResourceGroup.
Cada marca tem um nome.
Os valores são opcionais.
Uma marca predefinida do Azure pode ter vários valores, mas quando você aplica a marca a um grupo de recursos ou recursos, aplica o nome da marca e apenas um de seus valores.
Por exemplo, você pode criar uma marca de Departamento predefinida com um valor para cada departamento, como Finanças, Recursos Humanos e TI.
Quando você aplica a marca Departamento a um recurso, aplica apenas um valor predefinido, como Finanças.

**CreateByResourceIdParameterSet:** o cmdlet **New-AzTag** com **um ResourceId** cria ou atualiza todo o conjunto de marcas em um recurso ou assinatura.
Esta operação permite adicionar ou substituir todo o conjunto de marcas no recurso ou assinatura especificado. A entidade especificada pode ter no máximo 50 marcas.

## Exemplos

### Exemplo 1: Criar uma marca predefinida
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Esse comando cria uma marca predefinida chamada FY2015.
Essa marca não tem valores.
Você pode aplicar uma marca sem valores a um grupo de recursos ou recursos ou usar **o New-AzTag** para adicionar valores à marca.
Você também pode especificar um valor ao aplicar a marca ao grupo de recursos ou recursos.

### Exemplo 2: Criar uma marca predefinida com um valor
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Esse comando cria uma marca predefinida chamada Departamento com um valor de Finanças.

### Exemplo 3: Adicionar um valor a uma marca predefinida
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Esses comandos criam uma marca predefinida chamada Departamento com dois valores.
Se o nome da marca existir, **o Novo-AzTag** adiciona o valor à marca existente em vez de criar uma nova.

### Exemplo 4: Usar uma marca predefinida
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

Os comandos neste exemplo criam e usam uma marca predefinida.

### Exemplo 5: cria ou atualiza todo o conjunto de marcas em uma assinatura

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Esse comando cria ou atualiza todo o conjunto de marcas na assinatura com {subId}.

### Exemplo 6: cria ou atualiza todo o conjunto de marcas em um recurso

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Esse comando cria ou atualiza todo o conjunto de marcas no recurso com {resourceId}.

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

### -Nome
Especifica o nome da marca predefinido.
Para criar uma nova marca predefinida, insira um nome exclusivo.
Para adicionar um valor a uma marca existente, insira o nome da marca existente.
Se uma marca predefinida existente tiver o nome especificado, o **Novo-AzTag** adiciona o valor especificado, se for o caso, à marca com esse nome em vez de criar uma nova marca.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valor
Especifica um valor de marca predefinido.
Marcas predefinidos podem ter vários valores, mas você pode inserir apenas um valor em cada comando.
Esse parâmetro é opcional, pois as marcas podem ter nomes sem valores.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
O identificador de recurso da entidade que está sendo marcada. Um recurso, um grupo de recursos ou uma assinatura podem ser marcados.

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
As marcas a colocar no recurso.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

### System.Collections.Hashtable

## Saídas

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## Notas

## LINKS RELACIONADOS

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)