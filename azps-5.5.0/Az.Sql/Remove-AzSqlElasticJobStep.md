---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110923"
---
# <span data-ttu-id="c1340-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="c1340-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="c1340-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1340-102">SYNOPSIS</span></span>
<span data-ttu-id="c1340-103">Remove a etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="c1340-103">Removes the job step</span></span>

## <span data-ttu-id="c1340-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1340-104">SYNTAX</span></span>

### <span data-ttu-id="c1340-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c1340-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1340-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="c1340-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1340-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c1340-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1340-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1340-108">DESCRIPTION</span></span>
<span data-ttu-id="c1340-109">O Remove-AzSqlElasticJobStep cmdlet remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="c1340-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="c1340-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1340-110">EXAMPLES</span></span>

### <span data-ttu-id="c1340-111">Exemplo 1: remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="c1340-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="c1340-112">Remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="c1340-112">Removes a job step from a job</span></span>

### <span data-ttu-id="c1340-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c1340-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="c1340-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1340-114">PARAMETERS</span></span>

### <span data-ttu-id="c1340-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c1340-115">-AgentName</span></span>
<span data-ttu-id="c1340-116">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="c1340-116">The agent name</span></span>

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

### <span data-ttu-id="c1340-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1340-117">-DefaultProfile</span></span>
<span data-ttu-id="c1340-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1340-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1340-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1340-119">-InputObject</span></span>
<span data-ttu-id="c1340-120">O objeto de entrada da etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="c1340-120">The job step input object</span></span>

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

### <span data-ttu-id="c1340-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="c1340-121">-JobName</span></span>
<span data-ttu-id="c1340-122">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="c1340-122">The job name</span></span>

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

### <span data-ttu-id="c1340-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1340-123">-Name</span></span>
<span data-ttu-id="c1340-124">O nome da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="c1340-124">The job step name</span></span>

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

### <span data-ttu-id="c1340-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1340-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1340-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c1340-126">The resource group name</span></span>

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

### <span data-ttu-id="c1340-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1340-127">-ResourceId</span></span>
<span data-ttu-id="c1340-128">A ID do recurso de etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="c1340-128">The job step resource id</span></span>

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

### <span data-ttu-id="c1340-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c1340-129">-ServerName</span></span>
<span data-ttu-id="c1340-130">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="c1340-130">The server name</span></span>

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

### <span data-ttu-id="c1340-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c1340-131">-Confirm</span></span>
<span data-ttu-id="c1340-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1340-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1340-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1340-133">-WhatIf</span></span>
<span data-ttu-id="c1340-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c1340-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1340-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1340-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1340-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1340-136">CommonParameters</span></span>
<span data-ttu-id="c1340-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1340-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1340-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1340-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1340-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1340-139">INPUTS</span></span>

### <span data-ttu-id="c1340-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticStepModel</span><span class="sxs-lookup"><span data-stu-id="c1340-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c1340-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1340-141">OUTPUTS</span></span>

### <span data-ttu-id="c1340-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticStepModel</span><span class="sxs-lookup"><span data-stu-id="c1340-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c1340-143">Notas</span><span class="sxs-lookup"><span data-stu-id="c1340-143">NOTES</span></span>

## <span data-ttu-id="c1340-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1340-144">RELATED LINKS</span></span>
