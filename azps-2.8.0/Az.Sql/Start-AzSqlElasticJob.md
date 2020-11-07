---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 13e6a0bd8a4934df4d0426de38d7a56ddd5af19b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773947"
---
# <span data-ttu-id="e1683-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="e1683-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="e1683-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1683-102">SYNOPSIS</span></span>
<span data-ttu-id="e1683-103">Inicia um trabalho, retornando uma ID de execução de trabalho que pode ser sondada para exibir seu status</span><span class="sxs-lookup"><span data-stu-id="e1683-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="e1683-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1683-104">SYNTAX</span></span>

### <span data-ttu-id="e1683-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="e1683-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1683-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e1683-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1683-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="e1683-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1683-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1683-108">DESCRIPTION</span></span>
<span data-ttu-id="e1683-109">O cmdlet Start-AzSqlElasticJob inicia um trabalho que retorna uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="e1683-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="e1683-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1683-110">EXAMPLES</span></span>

### <span data-ttu-id="e1683-111">Exemplo 1-inicia um trabalho que retorna uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="e1683-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="e1683-112">Inicia um trabalho que retorna uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="e1683-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="e1683-113">OS</span><span class="sxs-lookup"><span data-stu-id="e1683-113">PARAMETERS</span></span>

### <span data-ttu-id="e1683-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e1683-114">-AgentName</span></span>
<span data-ttu-id="e1683-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="e1683-115">The agent name</span></span>

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

### <span data-ttu-id="e1683-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1683-116">-AsJob</span></span>
<span data-ttu-id="e1683-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e1683-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1683-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1683-118">-DefaultProfile</span></span>
<span data-ttu-id="e1683-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1683-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1683-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="e1683-120">-JobName</span></span>
<span data-ttu-id="e1683-121">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="e1683-121">The job name</span></span>

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

### <span data-ttu-id="e1683-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e1683-122">-ParentObject</span></span>
<span data-ttu-id="e1683-123">O objeto de trabalho</span><span class="sxs-lookup"><span data-stu-id="e1683-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1683-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e1683-124">-ParentResourceId</span></span>
<span data-ttu-id="e1683-125">A ID do recurso do trabalho</span><span class="sxs-lookup"><span data-stu-id="e1683-125">The job resource id</span></span>

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

### <span data-ttu-id="e1683-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1683-126">-ResourceGroupName</span></span>
<span data-ttu-id="e1683-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e1683-127">The resource group name</span></span>

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

### <span data-ttu-id="e1683-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e1683-128">-ServerName</span></span>
<span data-ttu-id="e1683-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="e1683-129">The server name</span></span>

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

### <span data-ttu-id="e1683-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="e1683-130">-Wait</span></span>
<span data-ttu-id="e1683-131">O sinalizador de espera para indicar que você deve aguardar até que a execução do trabalho seja concluída</span><span class="sxs-lookup"><span data-stu-id="e1683-131">The wait flag to indicate to wait until the job's execution is done</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1683-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1683-132">-Confirm</span></span>
<span data-ttu-id="e1683-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1683-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1683-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1683-134">-WhatIf</span></span>
<span data-ttu-id="e1683-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1683-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1683-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1683-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1683-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1683-137">CommonParameters</span></span>
<span data-ttu-id="e1683-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1683-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1683-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1683-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1683-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1683-140">INPUTS</span></span>

### <span data-ttu-id="e1683-141">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="e1683-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="e1683-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1683-142">OUTPUTS</span></span>

### <span data-ttu-id="e1683-143">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="e1683-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e1683-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1683-144">NOTES</span></span>

## <span data-ttu-id="e1683-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1683-145">RELATED LINKS</span></span>

## <span data-ttu-id="e1683-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1683-146">RELATED LINKS</span></span>
