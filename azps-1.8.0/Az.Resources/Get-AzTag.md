---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: ce672284a3d9887fe52c33081f04a86e1e072405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599410"
---
# Get-AzTag

## Sinopse
Obtém marcas predefinidas do Azure.

## SYNTAX

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzTag** tem marcas predefinidas do Azure na sua assinatura.
Esse cmdlet retorna informações básicas sobre as marcas ou informações detalhadas sobre marcas e seus valores.
Todos os objetos de saída incluem uma propriedade Count que representa o número de recursos e grupos de recursos aos quais as marcas e os valores foram aplicados.
O módulo de marcas do Azure que **Get-AzTag** é parte de pode ajudá-lo a gerenciar marcas predefinidas do Azure.
Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.
Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.
Para criar uma marca predefinida, use o cmdlet New-AzTag.
Para aplicar uma marca predefinida a um grupo de recursos, use o parâmetro *tag* do cmdlet New-AzTag.
Para pesquisar grupos de recursos para um nome de marca ou nome ou valor específico, use o parâmetro *tag* do cmdlet Get-AzResourceGroup.

## EXEMPLOS

### Exemplo 1: obter todas as marcas predefinidas
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Este comando obtém todas as marcas predefinidas na assinatura.
A propriedade Count mostra quantas vezes a marca foi aplicada a recursos e grupos de recursos na assinatura.

### Exemplo 2: obter uma marca por nome
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Esse comando obtém informações detalhadas sobre a marca do departamento e seus valores.
A propriedade Count mostra quantas vezes a marca e cada um dos seus valores foram aplicados a recursos e grupos de recursos na assinatura.

### Exemplo 3: obter valores de todas as marcas
```
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Esse comando usa o parâmetro *detalhado* para obter informações detalhadas sobre todas as marcas predefinidas na assinatura.
Usar o parâmetro *detailed* é o equivalente a usar o parâmetro *Name* para cada marca.

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

### -Detalhado
Indica que essa operação adiciona informações sobre valores de marca à saída.

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

### -Nome
Especifica o nome da marca a ser obtida.
Por padrão, **Get-AzTag** Obtém informações básicas sobre todas as marcas predefinidas na assinatura.
Quando você especifica o parâmetro *Name* , o parâmetro *detalhado* não tem efeito.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. Management. Automation. SwitchParameter

## EXIBE

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag

## INFORMA

## LINKS RELACIONADOS

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)


