---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 788817dd9ca344501dc25bad48b71b7e24b653d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885784"
---
# <span data-ttu-id="04df1-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="04df1-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="04df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04df1-102">SYNOPSIS</span></span>
<span data-ttu-id="04df1-103">Remove a etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="04df1-103">Removes the job step</span></span>

## <span data-ttu-id="04df1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="04df1-104">SYNTAX</span></span>

### <span data-ttu-id="04df1-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="04df1-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04df1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="04df1-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04df1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="04df1-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04df1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="04df1-108">DESCRIPTION</span></span>
<span data-ttu-id="04df1-109">O Remove-AzSqlElasticJobStep cmdlet remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="04df1-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="04df1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04df1-110">EXAMPLES</span></span>

### <span data-ttu-id="04df1-111">Exemplo 1: remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="04df1-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="04df1-112">Remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="04df1-112">Removes a job step from a job</span></span>

### <span data-ttu-id="04df1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="04df1-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="04df1-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="04df1-114">PARAMETERS</span></span>

### <span data-ttu-id="04df1-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="04df1-115">-AgentName</span></span>
<span data-ttu-id="04df1-116">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="04df1-116">The agent name</span></span>

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

### <span data-ttu-id="04df1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04df1-117">-DefaultProfile</span></span>
<span data-ttu-id="04df1-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04df1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04df1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04df1-119">-InputObject</span></span>
<span data-ttu-id="04df1-120">O objeto de entrada da etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="04df1-120">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04df1-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="04df1-121">-JobName</span></span>
<span data-ttu-id="04df1-122">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="04df1-122">The job name</span></span>

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

### <span data-ttu-id="04df1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="04df1-123">-Name</span></span>
<span data-ttu-id="04df1-124">O nome da etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="04df1-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04df1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04df1-125">-ResourceGroupName</span></span>
<span data-ttu-id="04df1-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="04df1-126">The resource group name</span></span>

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

### <span data-ttu-id="04df1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04df1-127">-ResourceId</span></span>
<span data-ttu-id="04df1-128">A ID do recurso de etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="04df1-128">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04df1-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="04df1-129">-ServerName</span></span>
<span data-ttu-id="04df1-130">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="04df1-130">The server name</span></span>

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

### <span data-ttu-id="04df1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04df1-131">-Confirm</span></span>
<span data-ttu-id="04df1-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04df1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04df1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04df1-133">-WhatIf</span></span>
<span data-ttu-id="04df1-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04df1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04df1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04df1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04df1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04df1-136">CommonParameters</span></span>
<span data-ttu-id="04df1-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04df1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04df1-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04df1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04df1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04df1-139">INPUTS</span></span>

### <span data-ttu-id="04df1-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="04df1-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="04df1-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="04df1-141">OUTPUTS</span></span>

### <span data-ttu-id="04df1-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="04df1-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="04df1-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="04df1-143">NOTES</span></span>

## <span data-ttu-id="04df1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04df1-144">RELATED LINKS</span></span>
