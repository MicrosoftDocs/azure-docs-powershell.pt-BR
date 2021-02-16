---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113331"
---
# Get-AzResourceGroupDeployment

## Sinopse
Obtém as implantações em um grupo de recursos.

## Sintaxe

### GetByResourceGroupDeploymentName (Padrão)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzResourceGroupDeployment** obtém as implantações em um grupo de recursos do Azure.
*Especifique o* parâmetro Nome ou *ID* para filtrar os resultados.
Por padrão, **Get-AzResourceGroupDeployment** obtém todas as implantações para um grupo de recursos especificado.
Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, um banco de dados ou um site da Web.
Um grupo de recursos do Azure é um conjunto de recursos do Azure implantados como uma unidade.
Uma implantação é a operação que disponibiliza os recursos no grupo de recursos para uso.
Para obter mais informações sobre recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzResourceGroup dados.
Você pode usar esse cmdlet para acompanhamento.
Para depuração, use este cmdlet com Get-AzLog cmdlet.

## Exemplos

### Exemplo 1: Obter todas as implantações para um grupo de recursos
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Esse comando obtém todas as implantações do grupo de recursos ContosoLabsRG.
A saída mostra uma implantação para um blog do WordPress que usou um modelo de galeria.

### Exemplo 2: Obter uma implantação por nome
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Esse comando obtém a implantação DeployWebsite01 do grupo de recursos ContosoLabsRG.
Você pode atribuir um nome a uma implantação quando a criar usando os cmdlets **New-AzResourceGroup** ou **New-AzResourceGroupDeployment.**
Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.

### Exemplo 3: Obter as implantações de todos os grupos de recursos
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Esse comando obtém todos os grupos de recursos em sua assinatura usando o cmdlet Get-AzResourceGroup dados.
O comando passa os grupos de recursos para o cmdlet atual usando o operador de pipeline.
O cmdlet atual obtém todas as implantações de todos os grupos de recursos da assinatura e passa os resultados para o cmdlet Format-Table para exibir seus valores de propriedade **ResourceGroupName,** **DeploymentName** e **ProvisioningState.**

## Parâmetros

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
Especifica a ID da implantação do grupo de recursos a ser obter.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da implantação a ser obter.
Caracteres curinga não são permitidos.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
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

### -ResourceGroupName
Especifica o nome de um grupo de recursos.
O cmdlet obtém as implantações do grupo de recursos especificado por esse parâmetro.
Caracteres curinga não são permitidos.
Esse parâmetro é necessário e você pode especificar apenas um grupo de recursos em cada comando.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment

## Notas

## LINKS RELACIONADOS

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Teste-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


