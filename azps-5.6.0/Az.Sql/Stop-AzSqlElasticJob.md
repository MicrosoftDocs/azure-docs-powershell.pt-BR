---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 1279366f07ce071e223aea1f7cc048403b9b4379
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890575"
---
# <span data-ttu-id="94566-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="94566-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="94566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94566-102">SYNOPSIS</span></span>
<span data-ttu-id="94566-103">Interrompe um trabalho, uma vez que sua id de execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="94566-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="94566-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="94566-104">SYNTAX</span></span>

### <span data-ttu-id="94566-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="94566-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94566-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="94566-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94566-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94566-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94566-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="94566-108">DESCRIPTION</span></span>
<span data-ttu-id="94566-109">O Stop-AzSqlElasticJob cmdlet interrompe um trabalho com uma execução em execução.</span><span class="sxs-lookup"><span data-stu-id="94566-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="94566-110">Retorna o status atual da execução do trabalho</span><span class="sxs-lookup"><span data-stu-id="94566-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="94566-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94566-111">EXAMPLES</span></span>

### <span data-ttu-id="94566-112">Exemplo 1: interrompe um trabalho com uma execução de trabalho em execução</span><span class="sxs-lookup"><span data-stu-id="94566-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="94566-113">Interrompe uma execução de trabalho e retorna seu status atual</span><span class="sxs-lookup"><span data-stu-id="94566-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="94566-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="94566-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="94566-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="94566-115">PARAMETERS</span></span>

### <span data-ttu-id="94566-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="94566-116">-AgentName</span></span>
<span data-ttu-id="94566-117">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="94566-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94566-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94566-118">-DefaultProfile</span></span>
<span data-ttu-id="94566-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94566-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94566-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="94566-120">-JobExecutionId</span></span>
<span data-ttu-id="94566-121">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="94566-121">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94566-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="94566-122">-JobName</span></span>
<span data-ttu-id="94566-123">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="94566-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94566-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="94566-124">-ParentObject</span></span>
<span data-ttu-id="94566-125">O objeto de banco de dados de controle do agente</span><span class="sxs-lookup"><span data-stu-id="94566-125">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94566-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="94566-126">-ParentResourceId</span></span>
<span data-ttu-id="94566-127">A ID do recurso de execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="94566-127">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94566-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94566-128">-ResourceGroupName</span></span>
<span data-ttu-id="94566-129">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="94566-129">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94566-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="94566-130">-ServerName</span></span>
<span data-ttu-id="94566-131">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="94566-131">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94566-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94566-132">-Confirm</span></span>
<span data-ttu-id="94566-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94566-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94566-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94566-134">-WhatIf</span></span>
<span data-ttu-id="94566-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94566-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94566-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94566-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94566-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94566-137">CommonParameters</span></span>
<span data-ttu-id="94566-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94566-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94566-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94566-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94566-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94566-140">INPUTS</span></span>

### <span data-ttu-id="94566-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="94566-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="94566-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="94566-142">OUTPUTS</span></span>

### <span data-ttu-id="94566-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="94566-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="94566-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="94566-144">NOTES</span></span>

## <span data-ttu-id="94566-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94566-145">RELATED LINKS</span></span>
