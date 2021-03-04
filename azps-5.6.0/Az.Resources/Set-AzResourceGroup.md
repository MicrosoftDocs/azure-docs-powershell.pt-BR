---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: f344c3cd08fb717d1229fb0abb4386c8a2d39d5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891092"
---
# Set-AzResourceGroup

## SYNOPSIS
Modifica um grupo de recursos.

## SINTAXE

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

## DESCRIPTION
O cmdlet **Set-AzResourceGroup** modifica as propriedades de um grupo de recursos.
Você pode usar esse cmdlet para adicionar, alterar ou excluir as marcas do Azure aplicadas a um grupo de recursos.
*Especifique o parâmetro Name* para identificar o grupo de recursos e o parâmetro *Tag* para modificar as marcas.
Não é possível usar esse cmdlet para alterar o nome de um grupo de recursos.

## EXEMPLOS

### Exemplo 1: Aplicar uma marca a um grupo de recursos
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Este comando aplica uma marca Department com um valor de IT a um grupo de recursos que não tem marcas existentes.

### Exemplo 2: Adicionar marcas a um grupo de recursos
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Este exemplo adiciona uma marca Status com um valor aprovado e uma marca FY2016 a um grupo de recursos que possui marcas existentes. Como as marcas especificadas substituem as marcas existentes, você deve incluir as marcas existentes na nova coleção de marcas ou você as perderá.
O primeiro comando obtém o grupo de recursos ContosoRG e usa o método dot para obter o valor de sua propriedade Tags. O comando armazena as marcas na variável $Tags.
O segundo comando obtém as marcas na $Tags variável.
O terceiro comando usa o operador de atribuição += para adicionar as marcas Status e FY2016 à matriz de marcas na variável $Tags.
O quarto comando usa o parâmetro *Tag* de **Set-AzResourceGroup** para aplicar as marcas na variável $Tags ao grupo de recursos ContosoRG.
O quinto comando obtém todas as marcas aplicadas ao grupo de recursos ContosoRG. A saída mostra que o grupo de recursos tem a marca Department e as duas novas marcas, Status e FY2015.

### Exemplo 3: Excluir todas as marcas de um grupo de recursos
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Este comando especifica o parâmetro *Tag com* um valor de tabela de hash vazio para excluir todas as marcas do grupo de recursos ContosoRG.

## PARÂMETROS

### -ApiVersion
Especifica a versão da API que é suportada pelo provedor de recursos.
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
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -Id
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

### -Name
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

### -Pre
Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.

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
Pares de valores-chave na forma de uma tabela de hash. Por exemplo: @{key0="value0";key1=$null;key2="value2"} Uma marca é um par de valores de nome que você pode criar e aplicar a recursos e grupos de recursos. Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro *Tag* de Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome ou nome e valor da marca. Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custos, ou para acompanhar anotações ou comentários sobre os recursos.
Para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos. Para excluir uma marca, insira uma tabela de hash com todas as marcas atualmente aplicadas ao grupo de recursos, de **Get-AzResourceGroup**, exceto pela marca que você deseja excluir. Para excluir todas as marcas de um grupo de recursos, especifique uma tabela de hash vazia: `@{}` .

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.Collections.Hashtable

## SAÍDAS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## NOTES

## LINKS RELACIONADOS

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
