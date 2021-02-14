---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111002"
---
# <span data-ttu-id="26676-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="26676-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="26676-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26676-102">SYNOPSIS</span></span>
<span data-ttu-id="26676-103">Inicia uma sessão de depuração de fluxo de dados no Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="26676-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="26676-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26676-104">SYNTAX</span></span>

### <span data-ttu-id="26676-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="26676-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26676-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="26676-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26676-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="26676-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26676-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="26676-108">DESCRIPTION</span></span>
<span data-ttu-id="26676-109">Esse comando de longa execução inicia uma sessão de depuração de fluxo de dados para os próximos comandos de depuração.</span><span class="sxs-lookup"><span data-stu-id="26676-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="26676-110">Esse comando pode ser anexado com uma definição de tempo de execução de integração para configurar o tamanho/tipo de cluster de sessão de depuração.</span><span class="sxs-lookup"><span data-stu-id="26676-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="26676-111">A sequência de comandos do PowerShell para fluxo de trabalho de depuração de fluxo de trabalho de fluxo de dados deve ser:</span><span class="sxs-lookup"><span data-stu-id="26676-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="26676-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="26676-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="26676-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="26676-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="26676-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repita esta etapa para diferentes comandos/destinos ou repita a etapa 2 a 3 para alterar o arquivo de pacote)</span><span class="sxs-lookup"><span data-stu-id="26676-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="26676-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="26676-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="26676-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26676-116">EXAMPLES</span></span>

### <span data-ttu-id="26676-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="26676-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="26676-118">Inicia uma sessão de depuração com o sinalizador AsJob.</span><span class="sxs-lookup"><span data-stu-id="26676-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="26676-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26676-119">PARAMETERS</span></span>

### <span data-ttu-id="26676-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26676-120">-AsJob</span></span>
<span data-ttu-id="26676-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="26676-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26676-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="26676-122">-DataFactory</span></span>
<span data-ttu-id="26676-123">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="26676-123">The data factory object.</span></span>

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

### <span data-ttu-id="26676-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="26676-124">-DataFactoryName</span></span>
<span data-ttu-id="26676-125">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="26676-125">The data factory name.</span></span>

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

### <span data-ttu-id="26676-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26676-126">-DefaultProfile</span></span>
<span data-ttu-id="26676-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26676-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26676-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="26676-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="26676-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="26676-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26676-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26676-130">-ResourceGroupName</span></span>
<span data-ttu-id="26676-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="26676-131">The resource group name.</span></span>

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

### <span data-ttu-id="26676-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26676-132">-ResourceId</span></span>
<span data-ttu-id="26676-133">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="26676-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="26676-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="26676-134">-Confirm</span></span>
<span data-ttu-id="26676-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26676-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26676-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26676-136">-WhatIf</span></span>
<span data-ttu-id="26676-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="26676-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26676-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26676-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26676-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26676-139">CommonParameters</span></span>
<span data-ttu-id="26676-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26676-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26676-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26676-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26676-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="26676-142">INPUTS</span></span>

### <span data-ttu-id="26676-143">System.String</span><span class="sxs-lookup"><span data-stu-id="26676-143">System.String</span></span>

### <span data-ttu-id="26676-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="26676-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="26676-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="26676-145">OUTPUTS</span></span>

### <span data-ttu-id="26676-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="26676-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="26676-147">Notas</span><span class="sxs-lookup"><span data-stu-id="26676-147">NOTES</span></span>
<span data-ttu-id="26676-148">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="26676-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26676-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26676-149">RELATED LINKS</span></span>

[<span data-ttu-id="26676-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="26676-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="26676-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="26676-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="26676-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="26676-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="26676-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="26676-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)