---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 688926d05b56234ce11d4524afdcce326c5e09e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773634"
---
# <span data-ttu-id="42942-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="42942-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="42942-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42942-102">SYNOPSIS</span></span>
<span data-ttu-id="42942-103">Obtém um ou mais trabalhos</span><span class="sxs-lookup"><span data-stu-id="42942-103">Gets one or more jobs</span></span>

## <span data-ttu-id="42942-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42942-104">SYNTAX</span></span>

### <span data-ttu-id="42942-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="42942-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42942-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="42942-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42942-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="42942-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42942-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42942-108">DESCRIPTION</span></span>
<span data-ttu-id="42942-109">O cmdlet Get-AzSqlElasticJob Obtém um ou mais trabalhos</span><span class="sxs-lookup"><span data-stu-id="42942-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="42942-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42942-110">EXAMPLES</span></span>

### <span data-ttu-id="42942-111">Exemplo 1-recebe um trabalho</span><span class="sxs-lookup"><span data-stu-id="42942-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="42942-112">Obtém um trabalho</span><span class="sxs-lookup"><span data-stu-id="42942-112">Gets a job</span></span>

## <span data-ttu-id="42942-113">OS</span><span class="sxs-lookup"><span data-stu-id="42942-113">PARAMETERS</span></span>

### <span data-ttu-id="42942-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="42942-114">-AgentName</span></span>
<span data-ttu-id="42942-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="42942-115">The agent name</span></span>

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

### <span data-ttu-id="42942-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42942-116">-DefaultProfile</span></span>
<span data-ttu-id="42942-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42942-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42942-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="42942-118">-Name</span></span>
<span data-ttu-id="42942-119">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="42942-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42942-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="42942-120">-ParentObject</span></span>
<span data-ttu-id="42942-121">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="42942-121">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42942-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="42942-122">-ParentResourceId</span></span>
<span data-ttu-id="42942-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="42942-123">The agent resource id</span></span>

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

### <span data-ttu-id="42942-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42942-124">-ResourceGroupName</span></span>
<span data-ttu-id="42942-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="42942-125">The resource group name</span></span>

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

### <span data-ttu-id="42942-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="42942-126">-ServerName</span></span>
<span data-ttu-id="42942-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="42942-127">The server name</span></span>

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

### <span data-ttu-id="42942-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42942-128">CommonParameters</span></span>
<span data-ttu-id="42942-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42942-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42942-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42942-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42942-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42942-131">INPUTS</span></span>

### <span data-ttu-id="42942-132">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="42942-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="42942-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42942-133">OUTPUTS</span></span>

### <span data-ttu-id="42942-134">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="42942-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="42942-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42942-135">NOTES</span></span>

## <span data-ttu-id="42942-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42942-136">RELATED LINKS</span></span>
