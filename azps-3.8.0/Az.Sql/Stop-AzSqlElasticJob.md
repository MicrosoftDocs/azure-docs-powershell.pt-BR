---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ff117dfee7f660845389bd62245be4ecfd53b2f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777964"
---
# <span data-ttu-id="5c146-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="5c146-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="5c146-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c146-102">SYNOPSIS</span></span>
<span data-ttu-id="5c146-103">Interrompe um trabalho de acordo com a ID de execução do trabalho</span><span class="sxs-lookup"><span data-stu-id="5c146-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="5c146-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c146-104">SYNTAX</span></span>

### <span data-ttu-id="5c146-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="5c146-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c146-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5c146-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c146-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="5c146-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c146-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c146-108">DESCRIPTION</span></span>
<span data-ttu-id="5c146-109">O cmdlet Stop-AzSqlElasticJob interrompe um trabalho com uma execução em execução.</span><span class="sxs-lookup"><span data-stu-id="5c146-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="5c146-110">Retorna o status atual da execução do trabalho</span><span class="sxs-lookup"><span data-stu-id="5c146-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="5c146-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c146-111">EXAMPLES</span></span>

### <span data-ttu-id="5c146-112">Exemplo 1-interrompe um trabalho com uma execução de trabalho em execução</span><span class="sxs-lookup"><span data-stu-id="5c146-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="5c146-113">Interrompe uma execução de trabalho em execução e retorna o status atual</span><span class="sxs-lookup"><span data-stu-id="5c146-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="5c146-114">OS</span><span class="sxs-lookup"><span data-stu-id="5c146-114">PARAMETERS</span></span>

### <span data-ttu-id="5c146-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5c146-115">-AgentName</span></span>
<span data-ttu-id="5c146-116">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="5c146-116">The agent name</span></span>

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

### <span data-ttu-id="5c146-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c146-117">-DefaultProfile</span></span>
<span data-ttu-id="5c146-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c146-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c146-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="5c146-119">-JobExecutionId</span></span>
<span data-ttu-id="5c146-120">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c146-120">The job execution id.</span></span>

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

### <span data-ttu-id="5c146-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="5c146-121">-JobName</span></span>
<span data-ttu-id="5c146-122">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="5c146-122">The job name</span></span>

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

### <span data-ttu-id="5c146-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5c146-123">-ParentObject</span></span>
<span data-ttu-id="5c146-124">O objeto de banco de dados controle de agente</span><span class="sxs-lookup"><span data-stu-id="5c146-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="5c146-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5c146-125">-ParentResourceId</span></span>
<span data-ttu-id="5c146-126">A ID do recurso de execução do trabalho</span><span class="sxs-lookup"><span data-stu-id="5c146-126">The job execution resource id</span></span>

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

### <span data-ttu-id="5c146-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c146-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c146-128">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5c146-128">The resource group name</span></span>

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

### <span data-ttu-id="5c146-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5c146-129">-ServerName</span></span>
<span data-ttu-id="5c146-130">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="5c146-130">The server name</span></span>

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

### <span data-ttu-id="5c146-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c146-131">-Confirm</span></span>
<span data-ttu-id="5c146-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c146-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c146-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c146-133">-WhatIf</span></span>
<span data-ttu-id="5c146-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c146-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c146-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c146-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c146-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c146-136">CommonParameters</span></span>
<span data-ttu-id="5c146-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c146-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c146-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c146-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c146-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c146-139">INPUTS</span></span>

### <span data-ttu-id="5c146-140">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="5c146-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="5c146-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c146-141">OUTPUTS</span></span>

### <span data-ttu-id="5c146-142">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="5c146-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="5c146-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c146-143">NOTES</span></span>

## <span data-ttu-id="5c146-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c146-144">RELATED LINKS</span></span>
