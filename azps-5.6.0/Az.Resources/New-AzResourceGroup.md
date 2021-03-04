---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892728"
---
# New-AzResourceGroup

## SYNOPSIS
Cria um grupo de recursos do Azure.

## SINTAXE

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzResourceGroup** cria um grupo de recursos do Azure.
Você pode criar um grupo de recursos usando apenas um nome e local e, em seguida, usar o cmdlet New-AzResource para criar recursos para adicionar ao grupo de recursos.
Para adicionar uma implantação a um grupo de recursos existente, use New-AzResourceGroupDeployment cmdlet. Para adicionar um recurso a um grupo de recursos existente, use o cmdlet **New-AzResource.** Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site. Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.

## EXEMPLOS

### Exemplo 1: Criar um grupo de recursos vazio
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Este comando cria um grupo de recursos que não tem recursos. Você pode usar os cmdlets **New-AzResource** ou **New-AzResourceGroupDeployment** para adicionar recursos e implantações a esse grupo de recursos.

### Exemplo 2: Criar um grupo de recursos vazio usando parâmetros posicionais
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Este comando cria um grupo de recursos que não tem recursos.

### Exemplo 3: Criar um grupo de recursos com marcas
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Este comando cria um grupo de recursos vazio. Este comando é o mesmo que o comando no Exemplo 1, exceto que ele atribui marcas ao grupo de recursos. A primeira marca, chamada Empty, pode ser usada para identificar grupos de recursos que não têm recursos. A segunda marca se chama Departamento e tem um valor de Marketing. Você pode usar uma marca como esta para categorizar grupos de recursos para administração ou orçamento.

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

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

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

### -Location
Especifica o local do grupo de recursos. Especifique um local do data center do Azure, como o Oeste dos EUA ou o Sudeste Asiático. Você pode colocar um grupo de recursos em qualquer local. O grupo de recursos não precisa estar no mesmo local que sua assinatura do Azure ou no mesmo local que seus recursos.
Para determinar qual local dá suporte a cada tipo de recurso, use o cmdlet Get-AzResourceProvider com o *parâmetro ProviderNamespace.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Especifica um nome para o grupo de recursos. O nome do recurso deve ser exclusivo na assinatura. Se um grupo de recursos que já tiver esse nome existir, o comando solicitará a confirmação antes de substituir o grupo de recursos existente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
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
Pares de valores-chave na forma de uma tabela de hash. Por exemplo: @{key0="value0";key1=$null;key2="value2"} Para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos.
Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro *Tag* de Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome de marca ou por nome e valor. Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custos, ou para acompanhar anotações ou comentários sobre os recursos.
Para obter suas marcas predefinidas, use o cmdlet Get-AzTag de usuário.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.Collections.Hashtable

## SAÍDAS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## NOTES

## LINKS RELACIONADOS

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
