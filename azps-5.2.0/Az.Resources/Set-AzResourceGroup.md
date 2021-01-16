---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261328"
---
# Set-AzResourceGroup

## Sinopse
Modifica um grupo de recursos.

## SYNTAX

### SetByResourceGroupName (padrão)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzResourceGroup** modifica as propriedades de um grupo de recursos.
Você pode usar esse cmdlet para adicionar, alterar ou excluir as marcas do Azure aplicadas a um grupo de recursos.
Especifique o parâmetro *Name* para identificar o grupo de recursos e o parâmetro de *marca* para modificar as marcas.
Você não pode usar esse cmdlet para alterar o nome de um grupo de recursos.

## EXEMPLOS

### Exemplo 1: aplicar uma marca a um grupo de recursos
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Esse comando aplica uma marca de departamento com um valor a um grupo de recursos que não tem marcas existentes.

### Exemplo 2: adicionar marcas a um grupo de recursos
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Este exemplo adiciona uma marca de status com um valor de approved e uma marca FY2016 a um grupo de recursos que tem marcas existentes. Como as marcas que você especifica substituem as marcas existentes, você deve incluir as marcas existentes na nova coleção de marcas ou perdê-las.
O primeiro comando obtém o grupo de recursos ContosoRG e usa o método dot para obter o valor de sua propriedade Tags. O comando armazena as marcas na variável $Tags.
O segundo comando obtém as marcas na variável $Tags.
O terceiro comando usa o operador de atribuição + = para adicionar as marcas status e FY2016 à matriz de marcas na variável $Tags.
O quarto comando usa o parâmetro de *marca* de **set-AzResourceGroup** para aplicar as marcas na variável $Tags para o grupo de recursos ContosoRG.
O quinto comando obtém todas as marcas aplicadas ao grupo de recursos ContosoRG. A saída mostra que o grupo de recursos tem a marca de departamento e as duas novas marcas, status e FY2015.

### Exemplo 3: excluir todas as marcas de um grupo de recursos
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Esse comando especifica o parâmetro de *marca* com um valor de tabela de hash vazio para excluir todas as marcas do grupo de recursos ContosoRG.

## OS

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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
Especifica a ID do grupo de recursos a ser modificada.

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

### -Pre
Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.

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

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"} uma marca é um par de nome-valor que você pode criar e aplicar a recursos e grupos de recursos. Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro de *marca* Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome ou nome da marca ou valor. Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos.
Para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos. Para excluir uma marca, insira uma tabela de hash com todas as marcas aplicadas atualmente ao grupo de recursos, do **Get-AzResourceGroup**, exceto para a marca que você deseja excluir. Para excluir todas as marcas de um grupo de recursos, especifique uma tabela de hash vazia: `@{}` .

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### System. Collections. Hashtable

## EXIBE

### Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceGroup

## INFORMA

## LINKS RELACIONADOS

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
