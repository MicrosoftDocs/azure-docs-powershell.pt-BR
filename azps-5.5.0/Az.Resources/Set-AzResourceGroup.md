---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112627"
---
# Set-AzResourceGroup

## Sinopse
Modifica um grupo de recursos.

## Sintaxe

### SetByResourceGroupName (Padrão)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O **cmdlet Set-AzResourceGroup** modifica as propriedades de um grupo de recursos.
Você pode usar esse cmdlet para adicionar, alterar ou excluir as marcas do Azure aplicadas a um grupo de recursos.
*Especifique o parâmetro* Nome para identificar o grupo de recursos e o parâmetro *Marca* para modificar as marcas.
Você não pode usar esse cmdlet para alterar o nome de um grupo de recursos.

## Exemplos

### Exemplo 1: Aplicar uma marca a um grupo de recursos
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Esse comando aplica uma marca Departamento com um valor de IT a um grupo de recursos que não tem marcas existentes.

### Exemplo 2: Adicionar marcas a um grupo de recursos
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Este exemplo adiciona uma marca status com um valor de Aprovado e uma marca FY2016 a um grupo de recursos que tem marcas existentes. Como as marcas especificadas substituem as marcas existentes, você deve incluir as marcas existentes na nova coleção de marcas ou perdê-las.
O primeiro comando obtém o grupo de recursos ContosoRG e usa o método de ponto para obter o valor de sua propriedade Marcas. O comando armazena as marcas na variável $Tags dados.
O segundo comando obtém as marcas na variável $Tags dados.
O terceiro comando usa o operador de atribuição += para adicionar as marcas Status e FY2016 à matriz de marcas na variável $Tags dados.
O quarto comando usa *o* parâmetro Tag do **Set-AzResourceGroup** para aplicar as marcas na variável $Tags ao grupo de recursos ContosoRG.
O quinto comando obtém todas as marcas aplicadas ao grupo de recursos ContosoRG. A saída mostra que o grupo de recursos tem a marca Departamento e as duas novas marcas, Status e FY2015.

### Exemplo 3: Excluir todas as marcas de um grupo de recursos
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Esse comando especifica o parâmetro *Marca* com um valor de tabela hash vazio para excluir todas as marcas do grupo de recursos ContosoRG.

## Parâmetros

### -ApiVersion
Especifica a versão da API com suporte do Provedor de Recursos.
Você pode especificar uma versão diferente da versão padrão.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ID
Especifica a ID do grupo de recursos a ser modificado.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do grupo de recursos a ser modificado.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pré-
Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.

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

### -Tag
Pares de valor-chave na forma de uma tabela hash. Por exemplo: @{key0="value0";key1=$null;key2="value2"} Uma marca é um par nome-valor que você pode criar e aplicar a recursos e grupos de recursos. Depois de atribuir marcas a recursos e  grupos, você pode usar o parâmetro Tag do Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome ou nome de marca e valor. Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para acompanhar anotações ou comentários sobre os recursos.
Para adicionar ou alterar uma marca, você deve substituir o conjunto de marcas do grupo de recursos. Para excluir uma marca, insira uma tabela hash com todas as marcas aplicadas no momento ao grupo de recursos, do **Get-AzResourceGroup,** exceto a marca que você deseja excluir. Para excluir todas as marcas de um grupo de recursos, especifique uma tabela hash vazia: `@{}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

### System.Collections.Hashtable

## Saídas

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## Notas

## LINKS RELACIONADOS

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
