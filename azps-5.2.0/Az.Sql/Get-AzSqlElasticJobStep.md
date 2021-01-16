---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259581"
---
# <span data-ttu-id="92c53-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="92c53-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="92c53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92c53-102">SYNOPSIS</span></span>
<span data-ttu-id="92c53-103">Obtém uma ou mais etapas do trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-103">Gets one or more job steps</span></span>

## <span data-ttu-id="92c53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92c53-104">SYNTAX</span></span>

### <span data-ttu-id="92c53-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="92c53-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92c53-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="92c53-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92c53-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="92c53-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92c53-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="92c53-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92c53-109">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="92c53-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92c53-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="92c53-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92c53-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92c53-111">DESCRIPTION</span></span>
<span data-ttu-id="92c53-112">O cmdlet Get-AzSqlElasticJobStep Obtém uma ou mais etapas do trabalho a partir de um trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="92c53-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92c53-113">EXAMPLES</span></span>

### <span data-ttu-id="92c53-114">Exemplo 1: Obtém uma etapa de trabalho a partir de um trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="92c53-115">Obtém uma etapa de trabalho a partir de um trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-115">Gets a job step from a job</span></span>

## <span data-ttu-id="92c53-116">OS</span><span class="sxs-lookup"><span data-stu-id="92c53-116">PARAMETERS</span></span>

### <span data-ttu-id="92c53-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="92c53-117">-AgentName</span></span>
<span data-ttu-id="92c53-118">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="92c53-118">The agent name</span></span>

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

### <span data-ttu-id="92c53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92c53-119">-DefaultProfile</span></span>
<span data-ttu-id="92c53-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92c53-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92c53-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="92c53-121">-JobName</span></span>
<span data-ttu-id="92c53-122">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-122">The job name</span></span>

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

### <span data-ttu-id="92c53-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="92c53-123">-Name</span></span>
<span data-ttu-id="92c53-124">O nome da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-124">The job step name</span></span>

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

### <span data-ttu-id="92c53-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="92c53-125">-ParentObject</span></span>
<span data-ttu-id="92c53-126">O objeto de entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-126">The job input object</span></span>

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

### <span data-ttu-id="92c53-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="92c53-127">-ParentResourceId</span></span>
<span data-ttu-id="92c53-128">A ID do recurso do trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-128">The job resource id</span></span>

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

### <span data-ttu-id="92c53-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c53-129">-ResourceGroupName</span></span>
<span data-ttu-id="92c53-130">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="92c53-130">The resource group name</span></span>

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

### <span data-ttu-id="92c53-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="92c53-131">-ServerName</span></span>
<span data-ttu-id="92c53-132">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="92c53-132">The server name</span></span>

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

### <span data-ttu-id="92c53-133">-Versão</span><span class="sxs-lookup"><span data-stu-id="92c53-133">-Version</span></span>
<span data-ttu-id="92c53-134">O nome da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="92c53-134">The job step name</span></span>

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

### <span data-ttu-id="92c53-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c53-135">CommonParameters</span></span>
<span data-ttu-id="92c53-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c53-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c53-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92c53-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c53-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92c53-138">INPUTS</span></span>

### <span data-ttu-id="92c53-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="92c53-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="92c53-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92c53-140">OUTPUTS</span></span>

### <span data-ttu-id="92c53-141">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="92c53-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="92c53-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92c53-142">NOTES</span></span>

## <span data-ttu-id="92c53-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92c53-143">RELATED LINKS</span></span>
