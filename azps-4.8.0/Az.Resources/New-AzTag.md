---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110964"
---
# New-AzTag

## Sinopse
Cria uma marca predefinida do Azure ou adiciona valores a uma marca existente | Cria ou atualiza todo o conjunto de marcas em um recurso ou assinatura.

## SYNTAX

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

## DESCRITIVO

**CreatePredefinedTagSet** : o cmdlet **New-AzTag** cria uma marca predefinida do Azure com um valor predefinido opcional.
Você também pode usá-lo para adicionar valores adicionais a marcas predefinidas existentes.
Para criar uma marca predefinida, insira um nome exclusivo para a marca.
Para adicionar um valor a uma marca predefinida existente, especifique o nome da marca existente e o novo valor.
Esse cmdlet retorna um objeto que representa a marca nova ou modificada com seus valores e o número de recursos aos quais ele foi aplicado.
O módulo de marcas do Azure que **New-AzTag** faz parte do pode ajudá-lo a gerenciar marcas predefinidas do Azure.
Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.
Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.
Para aplicar uma marca predefinida a um recurso ou grupo de recursos, use o parâmetro *tag* do cmdlet New-AzTag.
Para pesquisar grupos de recursos com um nome de marca ou nome ou valor especificado, use o parâmetro *tag* do cmdlet Get-AzResourceGroup.
Cada marca tem um nome.
Os valores são opcionais.
Uma marca predefinida do Azure pode ter vários valores, mas quando você aplica a marca a um recurso ou grupo de recursos, aplica o nome da marca e somente um de seus valores.
Por exemplo, você pode criar uma marca de departamento predefinida com um valor para cada departamento, como finanças, recursos humanos e isso.
Ao aplicar a marca de departamento a um recurso, você aplica apenas um valor predefinido, como finanças.

**CreateByResourceIdParameterSet** : o cmdlet **New-AzTag** com uma **ResourceId** cria ou atualiza todo o conjunto de marcas em um recurso ou assinatura.
Esta operação permite adicionar ou substituir o conjunto inteiro de marcas no recurso ou assinatura especificada. A entidade especificada pode ter no máximo 50 marcas.

## EXEMPLOS

### Exemplo 1: criar uma marca predefinida
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Esse comando cria uma marca predefinida chamada FY2015.
Esta marca não tem valores.
Você pode aplicar uma marca sem valores a um recurso ou grupo de recursos ou usar **New-AzTag** para adicionar valores à marca.
Você também pode especificar um valor ao aplicar a marca ao recurso ou grupo de recursos.

### Exemplo 2: criar uma marca predefinida com um valor
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Esse comando cria uma marca predefinida chamada Department com um valor de Finance.

### Exemplo 3: adicionar um valor a uma marca predefinida
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

Esses comandos criam uma marca predefinida chamada Department com dois valores.
Se o nome da marca existir, **New-AzTag** adiciona o valor à marca existente, em vez de criar uma nova.

### Exemplo 4: usar uma marca predefinida
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

Esse comando cria ou atualiza todo o conjunto de marcas no recurso com {ResourceId}.

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
Especifica o nome de marca predefinido.
Para criar uma nova marca predefinida, insira um nome exclusivo.
Para adicionar um valor a uma marca existente, insira o nome da marca existente.
Se uma marca predefinida existente tiver o nome especificado, **New-AzTag** adicionará o valor especificado, se houver, à marca com esse nome em vez de criar uma nova marca.

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
Marcas predefinidas podem ter vários valores, mas você pode inserir apenas um valor em cada comando.
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
O identificador de recurso para a entidade que está sendo marcada. Um recurso, um grupo de recursos ou uma assinatura pode estar marcado.

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

### -Marca
As marcas a serem colocadas no recurso.

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

### System. Collections. Hashtable

## EXIBE

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## INFORMA

## LINKS RELACIONADOS

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
