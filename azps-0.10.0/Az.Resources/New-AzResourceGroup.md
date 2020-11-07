---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: b0d9d23b9563c38a985adfa3d12dfc2854319512
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776389"
---
# New-AzResourceGroup

## Sinopse
Cria um grupo de recursos do Azure.

## SYNTAX

```
New-AzResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzResourceGroup** cria um grupo de recursos do Azure.
Você pode criar um grupo de recursos usando apenas um nome e um local e, em seguida, usar o cmdlet New-AzResource para criar recursos a serem adicionados ao grupo de recursos.
Para adicionar uma implantação a um grupo de recursos existente, use o cmdlet New-AzResourceGroupDeployment. Para adicionar um recurso a um grupo de recursos existente, use o cmdlet **New-AzResource** . Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site. Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.

## EXEMPLOS

### Exemplo 1: criar um grupo de recursos vazio
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Esse comando cria um grupo de recursos sem recursos. Você pode usar os cmdlets **New-AzResource** ou **New-AzResourceGroupDeployment** para adicionar recursos e implantações a este grupo de recursos.

### Exemplo 2: criar um grupo de recursos vazios usando parâmetros de posição
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Esse comando cria um grupo de recursos sem recursos.

### Exemplo 3: criar um grupo de recursos com marcas
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Esse comando cria um grupo de recursos vazios. Esse comando é o mesmo que o comando no exemplo 1, exceto que ele atribui marcas ao grupo de recursos. A primeira marca, denominada Empty, pode ser usada para identificar grupos de recursos que não têm recursos. A segunda marca é nomeada departamento e tem um valor de marketing. Você pode usar uma marca como esta para categorizar grupos de recursos para administração ou orçamento.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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

### -Local
Especifica o local do grupo de recursos. Especifique um local do Azure Data Center, como Oeste EUA ou sudeste asiático. Você pode colocar um grupo de recursos em qualquer local. O grupo de recursos não precisa estar no mesmo local de sua assinatura do Azure ou no mesmo local de seus recursos.
Para determinar qual local oferece suporte a cada tipo de recurso, use o cmdlet Get-AzResourceProvider com o parâmetro *ProviderNamespace* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica um nome para o grupo de recursos. O nome do recurso deve ser exclusivo na assinatura. Se um grupo de recursos com esse nome já existir, o comando solicitará confirmação antes de substituir o grupo de recursos existente.

```yaml
Type: System.String
Parameter Sets: (All)
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
Pares de valores chave na forma de uma tabela de hash. Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"} para adicionar ou alterar uma marca, você deve substituir a coleção de marcas do grupo de recursos.
Depois de atribuir marcas a recursos e grupos, você pode usar o parâmetro de *marca* Get-AzResource e Get-AzResourceGroup para pesquisar recursos e grupos por nome de marca ou por nome e valor. Você pode usar marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos.
Para obter suas marcas predefinidas, use o cmdlet Get-AzTag.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup

## INFORMA

## LINKS RELACIONADOS

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
