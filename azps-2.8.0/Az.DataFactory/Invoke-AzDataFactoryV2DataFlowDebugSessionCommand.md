---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 45419ede425b5d5ea3ba9fcbbbfb024fe8ba9358
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597040"
---
# <span data-ttu-id="8d6b0-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="8d6b0-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="8d6b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d6b0-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6b0-103">Invocar ação de depuração na sessão de depuração do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="8d6b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d6b0-104">SYNTAX</span></span>

### <span data-ttu-id="8d6b0-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d6b0-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d6b0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8d6b0-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d6b0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d6b0-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d6b0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d6b0-108">DESCRIPTION</span></span>
<span data-ttu-id="8d6b0-109">Este comando executa a visualização de dados/visualização de estatísticas/visualização de expressão para um fluxo de fluxo de dados diferente na sessão de depuração.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="8d6b0-110">A sequência de comandos do PowerShell para o fluxo de trabalho de depuração do fluxo de dados deve ser:</span><span class="sxs-lookup"><span data-stu-id="8d6b0-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="8d6b0-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d6b0-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="8d6b0-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="8d6b0-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="8d6b0-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repita esta etapa para diferentes comandos/destinos ou repita a etapa 2-3 para alterar o arquivo de pacote)</span><span class="sxs-lookup"><span data-stu-id="8d6b0-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="8d6b0-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d6b0-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="8d6b0-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d6b0-115">EXAMPLES</span></span>

### <span data-ttu-id="8d6b0-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d6b0-116">Example 1</span></span>
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

<span data-ttu-id="8d6b0-117">Este exemplo invoca o comando de visualização de dados para a sessão de depuração "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" na fábrica de dados "WiKiADF" e converte a saída JSON em cadeia de caracteres legível.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="8d6b0-118">OS</span><span class="sxs-lookup"><span data-stu-id="8d6b0-118">PARAMETERS</span></span>

### <span data-ttu-id="8d6b0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d6b0-119">-AsJob</span></span>
<span data-ttu-id="8d6b0-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8d6b0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d6b0-121">-Colunas</span><span class="sxs-lookup"><span data-stu-id="8d6b0-121">-Columns</span></span>
<span data-ttu-id="8d6b0-122">A lista de colunas para a visualização de estatísticas do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-122">The columns list for data flow statistics preview.</span></span>

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

### <span data-ttu-id="8d6b0-123">-Comando</span><span class="sxs-lookup"><span data-stu-id="8d6b0-123">-Command</span></span>
<span data-ttu-id="8d6b0-124">O comando de depuração do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-124">The data flow debug command.</span></span> <span data-ttu-id="8d6b0-125">As opções são executePreviewQuery, executeStatisticsQuery e executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="8d6b0-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="8d6b0-126">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="8d6b0-126">-DataFactory</span></span>
<span data-ttu-id="8d6b0-127">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-127">The data factory object.</span></span>

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

### <span data-ttu-id="8d6b0-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8d6b0-128">-DataFactoryName</span></span>
<span data-ttu-id="8d6b0-129">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-129">The data factory name.</span></span>

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

### <span data-ttu-id="8d6b0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6b0-130">-DefaultProfile</span></span>
<span data-ttu-id="8d6b0-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d6b0-132">-Expressão</span><span class="sxs-lookup"><span data-stu-id="8d6b0-132">-Expression</span></span>
<span data-ttu-id="8d6b0-133">A expressão para visualização da expressão do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-133">The expression for data flow expression preview.</span></span>

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

### <span data-ttu-id="8d6b0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d6b0-134">-ResourceGroupName</span></span>
<span data-ttu-id="8d6b0-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-135">The resource group name.</span></span>

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

### <span data-ttu-id="8d6b0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d6b0-136">-ResourceId</span></span>
<span data-ttu-id="8d6b0-137">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8d6b0-138">-Limites</span><span class="sxs-lookup"><span data-stu-id="8d6b0-138">-RowLimits</span></span>
<span data-ttu-id="8d6b0-139">O limite de linha para a visualização de dados do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-139">The row limit for data flow data preview.</span></span>

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

### <span data-ttu-id="8d6b0-140">-Identificação_da_sessão</span><span class="sxs-lookup"><span data-stu-id="8d6b0-140">-SessionId</span></span>
<span data-ttu-id="8d6b0-141">A ID da sessão de depuração do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-141">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="8d6b0-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="8d6b0-142">-StreamName</span></span>
<span data-ttu-id="8d6b0-143">O nome do fluxo do fluxo de dados para depuração.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-143">The stream name of data flow for debugging.</span></span>

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

### <span data-ttu-id="8d6b0-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d6b0-144">-Confirm</span></span>
<span data-ttu-id="8d6b0-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d6b0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d6b0-146">-WhatIf</span></span>
<span data-ttu-id="8d6b0-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d6b0-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d6b0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6b0-149">CommonParameters</span></span>
<span data-ttu-id="8d6b0-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d6b0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6b0-151">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d6b0-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6b0-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d6b0-152">INPUTS</span></span>

### <span data-ttu-id="8d6b0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8d6b0-153">System.String</span></span>

### <span data-ttu-id="8d6b0-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8d6b0-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8d6b0-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d6b0-155">OUTPUTS</span></span>

### <span data-ttu-id="8d6b0-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="8d6b0-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="8d6b0-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d6b0-157">NOTES</span></span>
<span data-ttu-id="8d6b0-158">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, factoriesKeywords: Azure, azurerm, ARM, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="8d6b0-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8d6b0-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d6b0-159">RELATED LINKS</span></span>

[<span data-ttu-id="8d6b0-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d6b0-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="8d6b0-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d6b0-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="8d6b0-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="8d6b0-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="8d6b0-163">Parar-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d6b0-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
