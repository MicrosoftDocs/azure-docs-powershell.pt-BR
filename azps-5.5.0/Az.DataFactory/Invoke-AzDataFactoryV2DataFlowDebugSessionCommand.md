---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116261"
---
# <span data-ttu-id="1bf26-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="1bf26-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="1bf26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bf26-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf26-103">Ação de depuração invocada na sessão de depuração de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="1bf26-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="1bf26-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bf26-104">SYNTAX</span></span>

### <span data-ttu-id="1bf26-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="1bf26-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bf26-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1bf26-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bf26-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf26-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf26-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bf26-108">DESCRIPTION</span></span>
<span data-ttu-id="1bf26-109">Esse comando executa visualização de dados/visualização de estatísticas/visualização de expressão para um fluxo diferente de fluxo de dados na sessão de depuração.</span><span class="sxs-lookup"><span data-stu-id="1bf26-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="1bf26-110">A sequência de comandos do PowerShell para fluxo de trabalho de depuração de fluxo de trabalho de fluxo de dados deve ser:</span><span class="sxs-lookup"><span data-stu-id="1bf26-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="1bf26-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1bf26-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="1bf26-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="1bf26-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="1bf26-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repita esta etapa para diferentes comandos/destinos ou repita a etapa 2 a 3 para alterar o arquivo de pacote)</span><span class="sxs-lookup"><span data-stu-id="1bf26-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="1bf26-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1bf26-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="1bf26-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1bf26-115">EXAMPLES</span></span>

### <span data-ttu-id="1bf26-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1bf26-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="1bf26-117">Este exemplo invoca o comando de visualização de dados para a sessão de depuração "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" no fábrica de dados "WiKiADF" e converta a saída JSON em cadeia de caracteres acessível.</span><span class="sxs-lookup"><span data-stu-id="1bf26-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="1bf26-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bf26-118">PARAMETERS</span></span>

### <span data-ttu-id="1bf26-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bf26-119">-AsJob</span></span>
<span data-ttu-id="1bf26-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1bf26-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bf26-121">-Colunas</span><span class="sxs-lookup"><span data-stu-id="1bf26-121">-Columns</span></span>
<span data-ttu-id="1bf26-122">A lista de colunas para visualização das estatísticas de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="1bf26-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-123">-Command</span><span class="sxs-lookup"><span data-stu-id="1bf26-123">-Command</span></span>
<span data-ttu-id="1bf26-124">O comando de depuração de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="1bf26-124">The data flow debug command.</span></span> <span data-ttu-id="1bf26-125">Os opcionais são executePreviewQuery, executeStatisticsQuery e executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="1bf26-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1bf26-126">-DataFactory</span></span>
<span data-ttu-id="1bf26-127">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1bf26-127">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1bf26-128">-DataFactoryName</span></span>
<span data-ttu-id="1bf26-129">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1bf26-129">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf26-130">-DefaultProfile</span></span>
<span data-ttu-id="1bf26-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf26-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf26-132">-Expressão</span><span class="sxs-lookup"><span data-stu-id="1bf26-132">-Expression</span></span>
<span data-ttu-id="1bf26-133">A expressão para visualização da expressão de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="1bf26-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf26-134">-ResourceGroupName</span></span>
<span data-ttu-id="1bf26-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1bf26-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf26-136">-ResourceId</span></span>
<span data-ttu-id="1bf26-137">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf26-137">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-138">-Delimitações de Linha</span><span class="sxs-lookup"><span data-stu-id="1bf26-138">-RowLimits</span></span>
<span data-ttu-id="1bf26-139">O limite de linha para a visualização de dados de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="1bf26-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="1bf26-140">-SessionId</span></span>
<span data-ttu-id="1bf26-141">A ID da sessão de depuração do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="1bf26-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="1bf26-142">-StreamName</span></span>
<span data-ttu-id="1bf26-143">O nome do fluxo do fluxo de dados para depuração.</span><span class="sxs-lookup"><span data-stu-id="1bf26-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf26-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1bf26-144">-Confirm</span></span>
<span data-ttu-id="1bf26-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bf26-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf26-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf26-146">-WhatIf</span></span>
<span data-ttu-id="1bf26-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1bf26-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bf26-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1bf26-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf26-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf26-149">CommonParameters</span></span>
<span data-ttu-id="1bf26-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf26-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf26-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bf26-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf26-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="1bf26-152">INPUTS</span></span>

### <span data-ttu-id="1bf26-153">System.String</span><span class="sxs-lookup"><span data-stu-id="1bf26-153">System.String</span></span>

### <span data-ttu-id="1bf26-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1bf26-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1bf26-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="1bf26-155">OUTPUTS</span></span>

### <span data-ttu-id="1bf26-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="1bf26-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="1bf26-157">Notas</span><span class="sxs-lookup"><span data-stu-id="1bf26-157">NOTES</span></span>
<span data-ttu-id="1bf26-158">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, keywordKeywords: azure, azurerm, arm, resource, management, manager, data, keyword</span><span class="sxs-lookup"><span data-stu-id="1bf26-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1bf26-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bf26-159">RELATED LINKS</span></span>

[<span data-ttu-id="1bf26-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1bf26-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="1bf26-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1bf26-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="1bf26-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="1bf26-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="1bf26-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1bf26-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
