---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256913"
---
# <span data-ttu-id="933c3-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="933c3-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="933c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="933c3-102">SYNOPSIS</span></span>
<span data-ttu-id="933c3-103">Inicia uma sessão de depuração do fluxo de dados no Azure data Factory</span><span class="sxs-lookup"><span data-stu-id="933c3-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="933c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="933c3-104">SYNTAX</span></span>

### <span data-ttu-id="933c3-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="933c3-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="933c3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="933c3-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="933c3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="933c3-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="933c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="933c3-108">DESCRIPTION</span></span>
<span data-ttu-id="933c3-109">Esse comando de execução longa inicia uma sessão de depuração de fluxo de dados para os comandos de depuração futuros.</span><span class="sxs-lookup"><span data-stu-id="933c3-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="933c3-110">Esse comando pode ser anexado a uma definição de tempo de execução de integração para configurar o tamanho/tipo do cluster de sessão de depuração.</span><span class="sxs-lookup"><span data-stu-id="933c3-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="933c3-111">A sequência de comandos do PowerShell para o fluxo de trabalho de depuração do fluxo de dados deve ser:</span><span class="sxs-lookup"><span data-stu-id="933c3-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="933c3-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="933c3-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="933c3-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="933c3-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="933c3-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repita esta etapa para diferentes comandos/destinos ou repita a etapa 2-3 para alterar o arquivo de pacote)</span><span class="sxs-lookup"><span data-stu-id="933c3-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="933c3-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="933c3-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="933c3-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="933c3-116">EXAMPLES</span></span>

### <span data-ttu-id="933c3-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="933c3-117">Example 1</span></span>
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

<span data-ttu-id="933c3-118">Inicia uma sessão de depuração com o sinalizador AsJob.</span><span class="sxs-lookup"><span data-stu-id="933c3-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="933c3-119">OS</span><span class="sxs-lookup"><span data-stu-id="933c3-119">PARAMETERS</span></span>

### <span data-ttu-id="933c3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="933c3-120">-AsJob</span></span>
<span data-ttu-id="933c3-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="933c3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="933c3-122">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="933c3-122">-DataFactory</span></span>
<span data-ttu-id="933c3-123">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="933c3-123">The data factory object.</span></span>

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

### <span data-ttu-id="933c3-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="933c3-124">-DataFactoryName</span></span>
<span data-ttu-id="933c3-125">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="933c3-125">The data factory name.</span></span>

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

### <span data-ttu-id="933c3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933c3-126">-DefaultProfile</span></span>
<span data-ttu-id="933c3-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="933c3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="933c3-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="933c3-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="933c3-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="933c3-129">The JSON file path.</span></span>

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

### <span data-ttu-id="933c3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933c3-130">-ResourceGroupName</span></span>
<span data-ttu-id="933c3-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="933c3-131">The resource group name.</span></span>

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

### <span data-ttu-id="933c3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="933c3-132">-ResourceId</span></span>
<span data-ttu-id="933c3-133">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="933c3-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="933c3-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="933c3-134">-Confirm</span></span>
<span data-ttu-id="933c3-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="933c3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="933c3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="933c3-136">-WhatIf</span></span>
<span data-ttu-id="933c3-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="933c3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="933c3-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="933c3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="933c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933c3-139">CommonParameters</span></span>
<span data-ttu-id="933c3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="933c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933c3-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="933c3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933c3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="933c3-142">INPUTS</span></span>

### <span data-ttu-id="933c3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="933c3-143">System.String</span></span>

### <span data-ttu-id="933c3-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="933c3-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="933c3-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="933c3-145">OUTPUTS</span></span>

### <span data-ttu-id="933c3-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="933c3-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="933c3-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="933c3-147">NOTES</span></span>
<span data-ttu-id="933c3-148">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="933c3-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="933c3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="933c3-149">RELATED LINKS</span></span>

[<span data-ttu-id="933c3-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="933c3-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="933c3-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="933c3-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="933c3-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="933c3-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="933c3-153">Parar-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="933c3-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)