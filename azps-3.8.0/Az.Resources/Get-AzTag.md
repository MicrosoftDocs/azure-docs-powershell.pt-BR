---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943780"
---
# Get-AzTag

## Sinopse
Obtém marcas predefinidas do Azure | Obtém todo o conjunto de marcas em um recurso ou assinatura.

## SYNTAX

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO

**GetPredefinedTagSet** : o cmdlet **Get-AzTag** Obtém marcas predefinidas do Azure na sua assinatura.
Esse cmdlet retorna informações básicas sobre as marcas ou informações detalhadas sobre marcas e seus valores.
Todos os objetos de saída incluem uma propriedade Count que representa o número de recursos e grupos de recursos aos quais as marcas e os valores foram aplicados.
O módulo de marcas do Azure que **Get-AzTag** é parte de pode ajudá-lo a gerenciar marcas predefinidas do Azure.
Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.
Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.
Para criar uma marca predefinida, use o cmdlet New-AzTag.
Para aplicar uma marca predefinida a um grupo de recursos, use o parâmetro *tag* do cmdlet New-AzTag.
Para pesquisar grupos de recursos para um nome de marca ou nome ou valor específico, use o parâmetro *tag* do cmdlet Get-AzResourceGroup.

**GetByResourceIdParameterSet** : o cmdlet **Get-AzTag** com uma **ResourceId** Obtém todo o conjunto de marcas em um recurso ou assinatura.

## EXEMPLOS

### Exemplo 1: obter todas as marcas predefinidas
```powershell
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
```powershell
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
```powershell
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

### Exemplo 4: obter o conjunto inteiro de marcas em uma assinatura

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Esse comando obtém todo o conjunto de marcas na assinatura com {subId}.

### Exemplo 5: obter o conjunto inteiro de marcas em um recurso

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Esse comando obtém todo o conjunto de marcas no recurso com {ResourceId}.

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
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome da marca predefinida.
Por padrão, **Get-AzTag** Obtém informações básicas sobre todas as marcas predefinidas na assinatura.
Quando você especifica o parâmetro *Name* , o parâmetro *detalhado* não tem efeito.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
O identificador de recurso para a entidade marcada. Um recurso, um grupo de recursos ou uma assinatura pode estar marcado.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### System. Management. Automation. SwitchParameter

## EXIBE

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## INFORMA

## LINKS RELACIONADOS

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
