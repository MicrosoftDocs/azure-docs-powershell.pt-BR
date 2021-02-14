---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115695"
---
# <span data-ttu-id="681a0-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="681a0-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="681a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="681a0-102">SYNOPSIS</span></span>
<span data-ttu-id="681a0-103">Inicia um trabalho, retornando uma ID de execução de trabalho que pode ser votada para exibir seu status</span><span class="sxs-lookup"><span data-stu-id="681a0-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="681a0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="681a0-104">SYNTAX</span></span>

### <span data-ttu-id="681a0-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="681a0-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="681a0-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="681a0-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="681a0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="681a0-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="681a0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="681a0-108">DESCRIPTION</span></span>
<span data-ttu-id="681a0-109">O Start-AzSqlElasticJob cmdlet inicia um trabalho retornando uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="681a0-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="681a0-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="681a0-110">EXAMPLES</span></span>

### <span data-ttu-id="681a0-111">Exemplo 1 - Inicia um trabalho retornando uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="681a0-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="681a0-112">Inicia um trabalho retornando uma nova execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="681a0-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="681a0-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="681a0-113">PARAMETERS</span></span>

### <span data-ttu-id="681a0-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="681a0-114">-AgentName</span></span>
<span data-ttu-id="681a0-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="681a0-115">The agent name</span></span>

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

### <span data-ttu-id="681a0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="681a0-116">-AsJob</span></span>
<span data-ttu-id="681a0-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="681a0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="681a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681a0-118">-DefaultProfile</span></span>
<span data-ttu-id="681a0-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="681a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="681a0-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="681a0-120">-JobName</span></span>
<span data-ttu-id="681a0-121">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="681a0-121">The job name</span></span>

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

### <span data-ttu-id="681a0-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="681a0-122">-ParentObject</span></span>
<span data-ttu-id="681a0-123">O objeto de trabalho</span><span class="sxs-lookup"><span data-stu-id="681a0-123">The job object</span></span>

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

### <span data-ttu-id="681a0-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="681a0-124">-ParentResourceId</span></span>
<span data-ttu-id="681a0-125">A ID do recurso de trabalho</span><span class="sxs-lookup"><span data-stu-id="681a0-125">The job resource id</span></span>

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

### <span data-ttu-id="681a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="681a0-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="681a0-127">The resource group name</span></span>

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

### <span data-ttu-id="681a0-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="681a0-128">-ServerName</span></span>
<span data-ttu-id="681a0-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="681a0-129">The server name</span></span>

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

### <span data-ttu-id="681a0-130">-Aguarde</span><span class="sxs-lookup"><span data-stu-id="681a0-130">-Wait</span></span>
<span data-ttu-id="681a0-131">O sinalizador de espera para indicar que aguarde até que a execução do trabalho seja feita</span><span class="sxs-lookup"><span data-stu-id="681a0-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="681a0-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="681a0-132">-Confirm</span></span>
<span data-ttu-id="681a0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="681a0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="681a0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="681a0-134">-WhatIf</span></span>
<span data-ttu-id="681a0-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="681a0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="681a0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="681a0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="681a0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681a0-137">CommonParameters</span></span>
<span data-ttu-id="681a0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="681a0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681a0-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="681a0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681a0-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="681a0-140">INPUTS</span></span>

### <span data-ttu-id="681a0-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="681a0-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="681a0-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="681a0-142">OUTPUTS</span></span>

### <span data-ttu-id="681a0-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="681a0-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="681a0-144">Notas</span><span class="sxs-lookup"><span data-stu-id="681a0-144">NOTES</span></span>

## <span data-ttu-id="681a0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="681a0-145">RELATED LINKS</span></span>
