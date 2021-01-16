---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257059"
---
# <span data-ttu-id="e70a1-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="e70a1-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="e70a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e70a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e70a1-103">Interrompe um trabalho de acordo com a ID de execução do trabalho</span><span class="sxs-lookup"><span data-stu-id="e70a1-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="e70a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e70a1-104">SYNTAX</span></span>

### <span data-ttu-id="e70a1-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="e70a1-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e70a1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e70a1-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70a1-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="e70a1-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70a1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e70a1-108">DESCRIPTION</span></span>
<span data-ttu-id="e70a1-109">O cmdlet Stop-AzSqlElasticJob interrompe um trabalho com uma execução em execução.</span><span class="sxs-lookup"><span data-stu-id="e70a1-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="e70a1-110">Retorna o status atual da execução do trabalho</span><span class="sxs-lookup"><span data-stu-id="e70a1-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="e70a1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e70a1-111">EXAMPLES</span></span>

### <span data-ttu-id="e70a1-112">Exemplo 1: interrompe um trabalho com uma execução de trabalho em execução</span><span class="sxs-lookup"><span data-stu-id="e70a1-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="e70a1-113">Interrompe uma execução de trabalho em execução e retorna o status atual</span><span class="sxs-lookup"><span data-stu-id="e70a1-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="e70a1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e70a1-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="e70a1-115">OS</span><span class="sxs-lookup"><span data-stu-id="e70a1-115">PARAMETERS</span></span>

### <span data-ttu-id="e70a1-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e70a1-116">-AgentName</span></span>
<span data-ttu-id="e70a1-117">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="e70a1-117">The agent name</span></span>

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

### <span data-ttu-id="e70a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70a1-118">-DefaultProfile</span></span>
<span data-ttu-id="e70a1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e70a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e70a1-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="e70a1-120">-JobExecutionId</span></span>
<span data-ttu-id="e70a1-121">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e70a1-121">The job execution id.</span></span>

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

### <span data-ttu-id="e70a1-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="e70a1-122">-JobName</span></span>
<span data-ttu-id="e70a1-123">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="e70a1-123">The job name</span></span>

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

### <span data-ttu-id="e70a1-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e70a1-124">-ParentObject</span></span>
<span data-ttu-id="e70a1-125">O objeto de banco de dados controle de agente</span><span class="sxs-lookup"><span data-stu-id="e70a1-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="e70a1-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e70a1-126">-ParentResourceId</span></span>
<span data-ttu-id="e70a1-127">A ID do recurso de execução do trabalho</span><span class="sxs-lookup"><span data-stu-id="e70a1-127">The job execution resource id</span></span>

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

### <span data-ttu-id="e70a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="e70a1-129">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e70a1-129">The resource group name</span></span>

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

### <span data-ttu-id="e70a1-130">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e70a1-130">-ServerName</span></span>
<span data-ttu-id="e70a1-131">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="e70a1-131">The server name</span></span>

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

### <span data-ttu-id="e70a1-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e70a1-132">-Confirm</span></span>
<span data-ttu-id="e70a1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e70a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e70a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70a1-134">-WhatIf</span></span>
<span data-ttu-id="e70a1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e70a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e70a1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e70a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e70a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70a1-137">CommonParameters</span></span>
<span data-ttu-id="e70a1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e70a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70a1-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e70a1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70a1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e70a1-140">INPUTS</span></span>

### <span data-ttu-id="e70a1-141">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="e70a1-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e70a1-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e70a1-142">OUTPUTS</span></span>

### <span data-ttu-id="e70a1-143">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="e70a1-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e70a1-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e70a1-144">NOTES</span></span>

## <span data-ttu-id="e70a1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e70a1-145">RELATED LINKS</span></span>
