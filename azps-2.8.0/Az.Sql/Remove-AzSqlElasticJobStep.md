---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 83d5733144c07c229cf8b5321ee9d3417ab112ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773813"
---
# <span data-ttu-id="2fd3b-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="2fd3b-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="2fd3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd3b-103">Remove a etapa trabalho</span><span class="sxs-lookup"><span data-stu-id="2fd3b-103">Removes the job step</span></span>

## <span data-ttu-id="2fd3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fd3b-104">SYNTAX</span></span>

### <span data-ttu-id="2fd3b-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="2fd3b-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fd3b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2fd3b-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fd3b-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="2fd3b-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fd3b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2fd3b-108">DESCRIPTION</span></span>
<span data-ttu-id="2fd3b-109">O cmdlet Remove-AzSqlElasticJobStep remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="2fd3b-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="2fd3b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fd3b-110">EXAMPLES</span></span>

### <span data-ttu-id="2fd3b-111">Exemplo 1-remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="2fd3b-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="2fd3b-112">Remove uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="2fd3b-112">Removes a job step from a job</span></span>

## <span data-ttu-id="2fd3b-113">OS</span><span class="sxs-lookup"><span data-stu-id="2fd3b-113">PARAMETERS</span></span>

### <span data-ttu-id="2fd3b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2fd3b-114">-AgentName</span></span>
<span data-ttu-id="2fd3b-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="2fd3b-115">The agent name</span></span>

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

### <span data-ttu-id="2fd3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd3b-116">-DefaultProfile</span></span>
<span data-ttu-id="2fd3b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fd3b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fd3b-118">-InputObject</span></span>
<span data-ttu-id="2fd3b-119">O objeto de entrada da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="2fd3b-119">The job step input object</span></span>

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

### <span data-ttu-id="2fd3b-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="2fd3b-120">-JobName</span></span>
<span data-ttu-id="2fd3b-121">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="2fd3b-121">The job name</span></span>

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

### <span data-ttu-id="2fd3b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fd3b-122">-Name</span></span>
<span data-ttu-id="2fd3b-123">O nome da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="2fd3b-123">The job step name</span></span>

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

### <span data-ttu-id="2fd3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fd3b-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2fd3b-125">The resource group name</span></span>

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

### <span data-ttu-id="2fd3b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fd3b-126">-ResourceId</span></span>
<span data-ttu-id="2fd3b-127">A ID do recurso etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="2fd3b-127">The job step resource id</span></span>

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

### <span data-ttu-id="2fd3b-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2fd3b-128">-ServerName</span></span>
<span data-ttu-id="2fd3b-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="2fd3b-129">The server name</span></span>

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

### <span data-ttu-id="2fd3b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2fd3b-130">-Confirm</span></span>
<span data-ttu-id="2fd3b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd3b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd3b-132">-WhatIf</span></span>
<span data-ttu-id="2fd3b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fd3b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd3b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd3b-135">CommonParameters</span></span>
<span data-ttu-id="2fd3b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd3b-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fd3b-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd3b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2fd3b-138">INPUTS</span></span>

### <span data-ttu-id="2fd3b-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2fd3b-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2fd3b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2fd3b-140">OUTPUTS</span></span>

### <span data-ttu-id="2fd3b-141">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2fd3b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2fd3b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2fd3b-142">NOTES</span></span>

## <span data-ttu-id="2fd3b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fd3b-143">RELATED LINKS</span></span>