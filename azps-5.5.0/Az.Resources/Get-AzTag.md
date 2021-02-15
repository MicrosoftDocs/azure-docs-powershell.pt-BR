---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118136"
---
# Get-AzTag

## Sinopse
Obtém marcas predefinidas do Azure | Obtém todo o conjunto de marcas em um recurso ou assinatura.

## Sintaxe

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição

**GetPredefinedTagSet:** o cmdlet **Get-AzTag** recebe marcas predefinidas do Azure em sua assinatura.
Este cmdlet retorna informações básicas sobre as marcas ou informações detalhadas sobre marcas e seus valores.
Todos os objetos de saída incluem uma propriedade Count que representa o número de recursos e grupos de recursos aos quais as marcas e valores foram aplicados.
O módulo Marcas do Azure do **que Get-AzTag** faz parte pode ajudá-lo a gerenciar marcas predefinidas do Azure.
Uma marca do Azure é um par de valores de nome que você pode usar para categorizar seus recursos e grupos de recursos do Azure, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.
Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinida permitem estabelecer nomes e valores padrão, consistentes e previsíveis para as marcas em sua assinatura.
Para criar uma marca predefinida, use New-AzTag cmdlet.
Para aplicar uma marca predefinida a um grupo de recursos, use o parâmetro *Tag* do cmdlet New-AzTag.
Para pesquisar em grupos de recursos um nome  ou nome e um valor de marca específicos, use o parâmetro Tag do cmdlet Get-AzResourceGroup dados.

**GetByResourceIdParameterSet:** o cmdlet **Get-AzTag** com **um ResourceId** obtém todo o conjunto de marcas em um recurso ou assinatura.

## Exemplos

### Exemplo 1: Obter todas as marcas predefinidos
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Esse comando obtém todas as marcas predefinida na assinatura.
A propriedade Count mostra quantas vezes a marca foi aplicada aos recursos e grupos de recursos na assinatura.

### Exemplo 2: Obter uma marca por nome
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

Este comando obtém informações detalhadas sobre a marca Departamento e seus valores.
A propriedade Count mostra quantas vezes a marca e cada um de seus valores foi aplicado a recursos e grupos de recursos na assinatura.

### Exemplo 3: Obter valores de todas as marcas
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

Esse comando usa o *parâmetro Detalhado* para obter informações detalhadas sobre todas as marcas predefinida na assinatura.
Usar o *parâmetro Detalhado* equivale a usar o parâmetro *Nome* para cada marca.

### Exemplo 4: Obter todo o conjunto de marcas em uma assinatura

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

### Exemplo 5: Obter todo o conjunto de marcas em um recurso

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

Esse comando obtém todo o conjunto de marcas no recurso com {resourceId}.

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
Por padrão, **o Get-AzTag** obtém informações básicas sobre todas as marcas predefinida na assinatura.
Quando você especifica o *parâmetro Nome,* o *parâmetro* Detalhado não tem efeito.

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
O identificador de recurso da entidade marcada. Um recurso, um grupo de recursos ou uma assinatura podem ser marcados.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

### System.Management.Automation.SwitchParameter

## Saídas

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## Notas

## LINKS RELACIONADOS

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
