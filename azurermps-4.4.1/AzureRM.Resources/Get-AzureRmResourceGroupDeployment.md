---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432578"
---
# Get-AzureRmResourceGroupDeployment

## Sinopse
Obtém as implantações em um grupo de recursos.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### O parâmetro de nome de implantação definido. Assume
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### O conjunto de parâmetros de ID de implantação.
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmResourceGroupDeployment** Obtém as implantações em um grupo de recursos do Azure.
Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.
Por padrão, **Get-AzureRmResourceGroupDeployment** obtém todas as implantações para um grupo de recursos especificado.

Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site da Web.
Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.

Uma implantação é a operação que torna os recursos do grupo de recursos disponíveis para uso.
Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzureRmResourceGroup.

Você pode usar esse cmdlet para acompanhamento.
Para a depuração, use esse cmdlet com o cmdlet Get-AzureRmLog.

## EXEMPLOS

### Exemplo 1: obter todas as implantações para um grupo de recursos
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Esse comando obtém todas as implantações para o grupo de recursos ContosoLabsRG.
A saída mostra uma implantação de um blog do WordPress que usava um modelo de galeria.

### Exemplo 2: obter uma implantação por nome
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Esse comando obtém a implantação do DeployWebsite01 do grupo de recursos ContosoLabsRG.
Você pode atribuir um nome a uma implantação ao criá-lo usando os cmdlets **New-AzureRmResourceGroup** ou **New-AzureRmResourceGroupDeployment** .
Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.

### Exemplo 3: obter as implantações de todos os grupos de recursos
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Esse comando obtém todos os grupos de recursos na sua assinatura usando o cmdlet Get-AzureRmResourceGroup.
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

### -ID
Especifica a ID da implantação do grupo de recursos a ser obtida.

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
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
Parameter Sets: The deployment name parameter set.
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
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroupDeployment
O cmdlet retorna implantações de grupo de recursos.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[New-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[New-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Parar-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


