---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114291"
---
# New-AzMlWebService

## Sinopse
Cria um novo serviço Web.

## Sintaxe

### CriarDeArquivo
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
Cria um serviço Web do Azure Machine Learning em um grupo de recursos existente.
Se houver um serviço Web com o mesmo nome no grupo de recursos, a chamada atuará como uma operação de atualização e o serviço Web existente será substituído.

## Exemplos

### Exemplo 1: Criar um novo serviço a partir de uma definição baseada em arquivo Json
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Cria um novo serviço Web do Azure Machine Learning chamado "mywebservicename" no grupo "myresourcegroup" e região da Central Sul dos EUA, com base na definição presente no arquivo json referenciado.

### Exemplo 2: Criar um novo serviço a partir de uma instância de objeto
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Você pode obter uma instância de objeto de serviço web para personalizar antes de publicar como um recurso usando o cmdlet Import-AzMlWebService web service.

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

### -DefinitionFile
Especifica o caminho para o arquivo que contém a definição de formato JSON do serviço Web.
Você pode encontrar a especificação mais recente para a definição do serviço Web na especificação de serviço web em https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Forçar
Não peça confirmação.

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
A região do serviço Web.
Insira uma região do data center do Azure, como "Oeste dos EUA" ou "Sudeste Asiático".
Você pode colocar um serviço Web em qualquer região que suporte recursos desse tipo.
O serviço Web não precisa estar na mesma região da sua assinatura do Azure ou na mesma região do grupo de recursos.
Os grupos de recursos podem conter serviços Web de regiões diferentes.
Para determinar quais regiões suportam cada tipo de recurso, use o Get-AzResourceProvider com o cmdlet de parâmetro ProviderNamespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome do serviço Web.
O nome deve ser exclusivo no grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
A definição do novo serviço Web, que contém todas as propriedades que comem o serviço.
Este parâmetro é necessário e representa uma instância da classe Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.
Você pode encontrar a especificação mais recente para a definição do serviço Web na especificação de serviço web em https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
O grupo de recursos no qual o serviço Web deve ser colocado.
Insira uma região do data center do Azure, como "Oeste dos EUA" ou "Sudeste Asiático".
Você pode colocar um serviço Web em qualquer região que suporte recursos desse tipo.
O serviço Web não precisa estar na mesma região da sua assinatura do Azure ou na mesma região do grupo de recursos.
Os grupos de recursos podem conter serviços Web de regiões diferentes.
Para determinar quais regiões suportam cada tipo de recurso, use o Get-AzResourceProvider com o cmdlet de parâmetro ProviderNamespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## Saídas

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## Notas
Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## LINKS RELACIONADOS
