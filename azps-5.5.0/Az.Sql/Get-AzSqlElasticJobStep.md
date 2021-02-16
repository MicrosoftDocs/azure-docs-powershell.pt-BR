---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116360"
---
# <span data-ttu-id="823bb-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="823bb-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="823bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="823bb-102">SYNOPSIS</span></span>
<span data-ttu-id="823bb-103">Obtém uma ou mais etapas de trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-103">Gets one or more job steps</span></span>

## <span data-ttu-id="823bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="823bb-104">SYNTAX</span></span>

### <span data-ttu-id="823bb-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="823bb-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="823bb-106">Getversion</span><span class="sxs-lookup"><span data-stu-id="823bb-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="823bb-107">Objectset</span><span class="sxs-lookup"><span data-stu-id="823bb-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="823bb-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="823bb-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="823bb-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="823bb-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="823bb-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="823bb-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="823bb-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="823bb-111">DESCRIPTION</span></span>
<span data-ttu-id="823bb-112">O Get-AzSqlElasticJobStep cmdlet obtém uma ou mais etapas de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="823bb-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="823bb-113">EXAMPLES</span></span>

### <span data-ttu-id="823bb-114">Exemplo 1: Obtém uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="823bb-115">Obtém uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-115">Gets a job step from a job</span></span>

## <span data-ttu-id="823bb-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="823bb-116">PARAMETERS</span></span>

### <span data-ttu-id="823bb-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="823bb-117">-AgentName</span></span>
<span data-ttu-id="823bb-118">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="823bb-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="823bb-119">-DefaultProfile</span></span>
<span data-ttu-id="823bb-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="823bb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="823bb-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="823bb-121">-JobName</span></span>
<span data-ttu-id="823bb-122">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823bb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="823bb-123">-Name</span></span>
<span data-ttu-id="823bb-124">O nome da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823bb-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="823bb-125">-ParentObject</span></span>
<span data-ttu-id="823bb-126">O objeto de entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="823bb-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="823bb-127">-ParentResourceId</span></span>
<span data-ttu-id="823bb-128">A ID do recurso de trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="823bb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="823bb-129">-ResourceGroupName</span></span>
<span data-ttu-id="823bb-130">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="823bb-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823bb-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="823bb-131">-ServerName</span></span>
<span data-ttu-id="823bb-132">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="823bb-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823bb-133">-Versão</span><span class="sxs-lookup"><span data-stu-id="823bb-133">-Version</span></span>
<span data-ttu-id="823bb-134">O nome da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="823bb-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="823bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="823bb-135">CommonParameters</span></span>
<span data-ttu-id="823bb-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="823bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="823bb-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="823bb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="823bb-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="823bb-138">INPUTS</span></span>

### <span data-ttu-id="823bb-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="823bb-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="823bb-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="823bb-140">OUTPUTS</span></span>

### <span data-ttu-id="823bb-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticStepModel</span><span class="sxs-lookup"><span data-stu-id="823bb-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="823bb-142">Notas</span><span class="sxs-lookup"><span data-stu-id="823bb-142">NOTES</span></span>

## <span data-ttu-id="823bb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="823bb-143">RELATED LINKS</span></span>
