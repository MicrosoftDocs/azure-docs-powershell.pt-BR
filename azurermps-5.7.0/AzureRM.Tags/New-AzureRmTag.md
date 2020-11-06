---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: 77bf93905b0cba4e8f8a23cb9f3cb8945fff74f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432855"
---
# New-AzureRmTag

## Sinopse
Cria uma marca predefinida do Azure ou adiciona valores a uma marca existente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmTag** cria uma marca predefinida do Azure com um valor predefinido opcional.
Você também pode usá-lo para adicionar valores adicionais a marcas predefinidas existentes.
Para criar uma marca predefinida, insira um nome exclusivo para a marca.
Para adicionar um valor a uma marca predefinida existente, especifique o nome da marca existente e o novo valor.

Esse cmdlet retorna um objeto que representa a marca nova ou modificada com seus valores e o número de recursos aos quais ele foi aplicado.

O módulo de marcas do Azure que **New-AzureRmTag** faz parte do pode ajudá-lo a gerenciar marcas predefinidas do Azure.
Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.

Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.
Se a assinatura incluir marcas predefinidas, não será possível aplicar marcas ou valores indefinidos a nenhum recurso ou grupo de recursos na assinatura.

Para aplicar uma marca predefinida a um recurso ou grupo de recursos, use o parâmetro *tag* do cmdlet New-AzureRmTag.
Para pesquisar grupos de recursos com um nome de marca ou nome ou valor especificado, use o parâmetro *tag* do cmdlet Get-AzureRMResourceGroup.

Cada marca tem um nome.
Os valores são opcionais.
Uma marca predefinida do Azure pode ter vários valores, mas quando você aplica a marca a um recurso ou grupo de recursos, aplica o nome da marca e somente um de seus valores.
Por exemplo, você pode criar uma marca de departamento predefinida com um valor para cada departamento, como finanças, recursos humanos e isso.
Ao aplicar a marca de departamento a um recurso, você aplica apenas um valor predefinido, como finanças.

## EXEMPLOS

### Exemplo 1: criar uma marca predefinida
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

Esse comando cria uma marca predefinida chamada FY2015.
Esta marca não tem valores.
Você pode aplicar uma marca sem valores a um recurso ou grupo de recursos ou usar **New-AzureRmTag** para adicionar valores à marca.
Você também pode especificar um valor ao aplicar a marca ao recurso ou grupo de recursos.

### Exemplo 2: criar uma marca predefinida com um valor
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Esse comando cria uma marca predefinida chamada Department com um valor de Finance.

### Exemplo 3: adicionar um valor a uma marca predefinida
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Esses comandos criam uma marca predefinida chamada Department com dois valores.
Se o nome da marca existir, **New-AzureRmTag** adiciona o valor à marca existente, em vez de criar uma nova.

### Exemplo 4: usar uma marca predefinida
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da marca.
Para criar uma nova marca predefinida, insira um nome exclusivo.

Para adicionar um valor a uma marca existente, insira o nome da marca existente.
Se uma marca predefinida existente tiver o nome especificado, **New-AzureRmTag** adicionará o valor especificado, se houver, à marca com esse nome em vez de criar uma nova marca.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valor
Especifica um valor de marca.
Marcas predefinidas podem ter vários valores, mas você pode inserir apenas um valor em cada comando.
Esse parâmetro é opcional, pois as marcas podem ter nomes sem valores.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Tags. Model. PSTag

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


