---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 75f94e5c93f81fa88dd33c3c0b94cb2b36ca291f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432197"
---
# Update-AzureRmMlWebService

## Sinopse
Atualiza as propriedades de um recurso de serviço Web existente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Atualize propriedades específicas do.
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Crie um novo Azure ML WebService a partir de uma definição de instância WebService.
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Update-AzureRmMlWebService permite que você atualize as propriedades não estáticas de um serviço Web.
O cmdlet funciona como uma operação de correção.
Passe apenas as propriedades que você deseja modificar.

## EXEMPLOS

### --------------------------Exemplo 1: argumentos de atualização seletiva--------------------------
@ {Paragraph = PS C: \\ \> }





```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

Aqui, alteramos a descrição, a chave de acesso primária e habilitamos a coleta de diagnósticos para todos os rastreamentos durante o tempo de execução para o serviço Web.

### --------------------------Exemplo 2: atualizar com base em uma instância de serviço Web--------------------------
@ {Paragraph = PS C: \\ \> }





```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

Primeiro, o exemplo cria uma definição de serviço Web, que contém somente os campos a serem atualizados e, em seguida, chama o Update-AzureRmMlWebService para aplicá-los usando o parâmetro service updates.

## OS

### -Ativos
O conjunto de ativos (por exemplo, módulos, conjuntos de valores) que compõem o serviço Web.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Descrição
O novo valor para a descrição do serviço Web.
Isso é visível no esquema de API do Swagger do serviço.

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diagnóstico
As configurações que controlam a coleção de rastreamentos de diagnóstico para o serviço Web.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
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

### -Entrada
A definição da (s) entrada (s) do serviço Web, fornecida como uma construção de esquema Swagger.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsReadOnly
Especifica que este serviço Web é muito ReadOnly.
Uma vez definido, o serviço Web pode ser mais atualizado, incluindo a alteração do valor dessa propriedade e só pode ser excluído.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Teclas
Atualiza uma ou ambas as teclas de acesso usadas para autenticar chamadas para as APIs de tempo de execução do serviço.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome do recurso de serviço Web a ser atualizado.

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

### -Saída
A definição da (s) saída (s) do serviço Web, fornecida como uma construção de esquema Swagger.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package
A definição do pacote de gráficos que define esse serviço Web.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parâmetros
O conjunto de valores de parâmetros globais definidos para o serviço Web, dado como um nome de parâmetro global- \> conjunto de valores padrão.
Se nenhum valor padrão for especificado, o parâmetro será considerado obrigatório.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RealtimeConfiguration
Atualizações para a configuração do ponto de extremidade em tempo real do serviço.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O grupo de recursos que contém o serviço Web a ser atualizado.

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

### -Atualizações
Um conjunto de atualizações a ser aplicado ao serviço Web fornecido como uma instância de definição de serviço Web.
Somente campos não estáticos são modificados.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountKey
Gira a tecla de acesso da conta de armazenamento associada ao serviço Web.

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Título
O novo valor para o título do serviço Web.
Isso é visível no esquema de API do Swagger do serviço.

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
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

### Serviço
O parâmetro ' unupdates ' aceita o valor do tipo ' WebService ' da pipeline

## EXIBE

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService
Uma descrição resumida do serviço Web do Azure Machine Learning.
Semelhante à descrição retornada chamando o cmdlet Get-AzureRmMlWebService em um serviço Web existente.
Essa descrição não contém propriedades confidenciais, como as credenciais da conta de armazenamento e as teclas de acesso do serviço.

## INFORMA
Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml

## LINKS RELACIONADOS

