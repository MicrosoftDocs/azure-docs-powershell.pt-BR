---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259876"
---
# <span data-ttu-id="f032b-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="f032b-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="f032b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f032b-102">SYNOPSIS</span></span>
<span data-ttu-id="f032b-103">Inicia um trabalho, retornando uma ID de execução de trabalho que pode ser sondada para exibir seu status</span><span class="sxs-lookup"><span data-stu-id="f032b-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="f032b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f032b-104">SYNTAX</span></span>

### <span data-ttu-id="f032b-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="f032b-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f032b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f032b-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f032b-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="f032b-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f032b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f032b-108">DESCRIPTION</span></span>
<span data-ttu-id="f032b-109">O cmdlet Start-AzSqlElasticJob inicia um trabalho que retorna uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="f032b-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="f032b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f032b-110">EXAMPLES</span></span>

### <span data-ttu-id="f032b-111">Exemplo 1-inicia um trabalho que retorna uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="f032b-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="f032b-112">Inicia um trabalho que retorna uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="f032b-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="f032b-113">OS</span><span class="sxs-lookup"><span data-stu-id="f032b-113">PARAMETERS</span></span>

### <span data-ttu-id="f032b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f032b-114">-AgentName</span></span>
<span data-ttu-id="f032b-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="f032b-115">The agent name</span></span>

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

### <span data-ttu-id="f032b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f032b-116">-AsJob</span></span>
<span data-ttu-id="f032b-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f032b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f032b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f032b-118">-DefaultProfile</span></span>
<span data-ttu-id="f032b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f032b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f032b-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="f032b-120">-JobName</span></span>
<span data-ttu-id="f032b-121">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="f032b-121">The job name</span></span>

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

### <span data-ttu-id="f032b-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f032b-122">-ParentObject</span></span>
<span data-ttu-id="f032b-123">O objeto de trabalho</span><span class="sxs-lookup"><span data-stu-id="f032b-123">The job object</span></span>

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

### <span data-ttu-id="f032b-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f032b-124">-ParentResourceId</span></span>
<span data-ttu-id="f032b-125">A ID do recurso do trabalho</span><span class="sxs-lookup"><span data-stu-id="f032b-125">The job resource id</span></span>

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

### <span data-ttu-id="f032b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f032b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f032b-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f032b-127">The resource group name</span></span>

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

### <span data-ttu-id="f032b-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f032b-128">-ServerName</span></span>
<span data-ttu-id="f032b-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="f032b-129">The server name</span></span>

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

### <span data-ttu-id="f032b-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="f032b-130">-Wait</span></span>
<span data-ttu-id="f032b-131">O sinalizador de espera para indicar que você deve aguardar até que a execução do trabalho seja concluída</span><span class="sxs-lookup"><span data-stu-id="f032b-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="f032b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f032b-132">-Confirm</span></span>
<span data-ttu-id="f032b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f032b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f032b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f032b-134">-WhatIf</span></span>
<span data-ttu-id="f032b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f032b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f032b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f032b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f032b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f032b-137">CommonParameters</span></span>
<span data-ttu-id="f032b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f032b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f032b-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f032b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f032b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f032b-140">INPUTS</span></span>

### <span data-ttu-id="f032b-141">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f032b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f032b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f032b-142">OUTPUTS</span></span>

### <span data-ttu-id="f032b-143">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="f032b-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="f032b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f032b-144">NOTES</span></span>

## <span data-ttu-id="f032b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f032b-145">RELATED LINKS</span></span>
