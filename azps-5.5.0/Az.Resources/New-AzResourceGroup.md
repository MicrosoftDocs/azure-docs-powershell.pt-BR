---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114899"
---
# New-AzResourceGroup

## Sinopse
Cria um grupo de recursos do Azure.

## Sintaxe

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O **cmdlet New-AzResourceGroup** cria um grupo de recursos do Azure.
Você pode criar um grupo de recursos usando apenas um nome e um local e, em seguida, usar o cmdlet New-AzResource para criar recursos para adicionar ao grupo de recursos.
Para adicionar uma implantação a um grupo de recursos existente, use o cmdlet New-AzResourceGroupDeployment dados. Para adicionar um recurso a um grupo de recursos existente, use o cmdlet **New-AzResource.** Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, um banco de dados ou um site. Um grupo de recursos do Azure é um conjunto de recursos do Azure implantados como uma unidade.

## Exemplos

### Exemplo 1: Criar um grupo de recursos vazio
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Esse comando cria um grupo de recursos que não tem recursos. Você pode usar os cmdlets **New-AzResource** ou **New-AzResourceGroupDeployment** para adicionar recursos e implantações a esse grupo de recursos.

### Exemplo 2: Criar um grupo de recursos vazio usando parâmetros posicionais
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Esse comando cria um grupo de recursos que não tem recursos.

### Exemplo 3: Criar um grupo de recursos com marcas
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Esse comando cria um grupo de recursos vazio. Esse comando é o mesmo que o comando no Exemplo 1, exceto que ele atribui marcas ao grupo de recursos. A primeira marca, chamada Vazia, pode ser usada para identificar grupos de recursos que não têm recursos. A segunda marca se chama Departamento e tem um valor de Marketing. Você pode usar uma marca como esta para categorizar grupos de recursos para administração ou orçamento.

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

### -Forçar
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

### -Local
Especifica o local do grupo de recursos. Especifique um local de data center do Azure, como Oeste dos EUA ou Sudeste Asiático. Você pode colocar um grupo de recursos em qualquer local. O grupo de recursos não precisa estar no mesmo local de sua assinatura do Azure ou no mesmo local que seus recursos.
Para determinar qual local dá suporte a cada tipo de recurso, use o cmdlet Get-AzResourceProvider com o parâmetro *ProviderNamespace.*

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

### -Nome
Especifica um nome para o grupo de recursos. O nome do recurso deve ser exclusivo na assinatura. Se um grupo de recursos que já tem esse nome já existir, o comando solicitará que você confirme antes de substituir o grupo de recursos existente.

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
Pares de valor-chave na forma de uma tabela hash. Por exemplo: @{key0="value0";key1=$null;key2="value2"} Para adicionar ou alterar uma marca, você deve substituir o conjunto de marcas do grupo de recursos.
Depois de atribuir marcas a recursos e  grupos, você pode usar o parâmetro Tag do Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome de marca ou por nome e valor. Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para acompanhar anotações ou comentários sobre os recursos.
Para obter suas marcas predefinidas, use o cmdlet Get-AzTag dados.

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

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## Notas

## LINKS RELACIONADOS

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
