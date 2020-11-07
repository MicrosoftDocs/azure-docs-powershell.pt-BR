---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948055"
---
# Get-AzResourceGroupDeployment

## Sinopse
Obtém as implantações em um grupo de recursos.

## SYNTAX

### GetByResourceGroupDeploymentName (padrão)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzResourceGroupDeployment** Obtém as implantações em um grupo de recursos do Azure.
Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.
Por padrão, **Get-AzResourceGroupDeployment** obtém todas as implantações para um grupo de recursos especificado.
Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site da Web.
Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.
Uma implantação é a operação que torna os recursos do grupo de recursos disponíveis para uso.
Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzResourceGroup.
Você pode usar esse cmdlet para acompanhamento.
Para a depuração, use esse cmdlet com o cmdlet Get-AzLog.

## EXEMPLOS

### Exemplo 1: obter todas as implantações para um grupo de recursos
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Esse comando obtém todas as implantações para o grupo de recursos ContosoLabsRG.
A saída mostra uma implantação de um blog do WordPress que usava um modelo de galeria.

### Exemplo 2: obter uma implantação por nome
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Esse comando obtém a implantação do DeployWebsite01 do grupo de recursos ContosoLabsRG.
Você pode atribuir um nome a uma implantação ao criá-lo usando os cmdlets **New-AzResourceGroup** ou **New-AzResourceGroupDeployment** .
Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.

### Exemplo 3: obter as implantações de todos os grupos de recursos
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Esse comando obtém todos os grupos de recursos na sua assinatura usando o cmdlet Get-AzResourceGroup.
O comando passa os grupos de recursos para o cmdlet atual usando o operador pipeline.
O cmdlet atual obtém todas as implantações de todos os grupos de recursos na assinatura e passa os resultados para o cmdlet Format-Table para exibir seus valores de propriedade **ResourceGroupName** , **deploymentname** e **ProvisioningState** .

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
Especifica a ID da implantação do grupo de recursos a ser obtida.

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
Especifica o nome da implantação a ser obtida.
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

### -ResourceGroupName
Especifica o nome de um grupo de recursos.
O cmdlet obtém as implantações do grupo de recursos que esse parâmetro especifica.
Caracteres curinga não são permitidos.
Esse parâmetro é obrigatório e você pode especificar apenas um grupo de recursos em cada comando.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceGroupDeployment

## INFORMA

## LINKS RELACIONADOS

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Parar-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


