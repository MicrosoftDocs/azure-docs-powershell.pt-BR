---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: 03f2e9af6b7225fd7622c03347bdea87c63453c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943191"
---
# <span data-ttu-id="6c47e-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="6c47e-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="6c47e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c47e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c47e-103">Remove um trabalho</span><span class="sxs-lookup"><span data-stu-id="6c47e-103">Removes a job</span></span>

## <span data-ttu-id="6c47e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c47e-104">SYNTAX</span></span>

### <span data-ttu-id="6c47e-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="6c47e-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c47e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6c47e-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c47e-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="6c47e-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c47e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c47e-108">DESCRIPTION</span></span>
<span data-ttu-id="6c47e-109">O cmdlet Remove-AzSqlElasticJob remove um trabalho</span><span class="sxs-lookup"><span data-stu-id="6c47e-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="6c47e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c47e-110">EXAMPLES</span></span>

### <span data-ttu-id="6c47e-111">Exemplo 1-remove um trabalho</span><span class="sxs-lookup"><span data-stu-id="6c47e-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="6c47e-112">Remove um trabalho</span><span class="sxs-lookup"><span data-stu-id="6c47e-112">Removes a job</span></span>

## <span data-ttu-id="6c47e-113">OS</span><span class="sxs-lookup"><span data-stu-id="6c47e-113">PARAMETERS</span></span>

### <span data-ttu-id="6c47e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6c47e-114">-AgentName</span></span>
<span data-ttu-id="6c47e-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="6c47e-115">The agent name</span></span>

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

### <span data-ttu-id="6c47e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c47e-116">-DefaultProfile</span></span>
<span data-ttu-id="6c47e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c47e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c47e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6c47e-118">-Force</span></span>
<span data-ttu-id="6c47e-119">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="6c47e-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6c47e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c47e-120">-InputObject</span></span>
<span data-ttu-id="6c47e-121">O objeto de entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="6c47e-121">The job input object</span></span>

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

### <span data-ttu-id="6c47e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c47e-122">-Name</span></span>
<span data-ttu-id="6c47e-123">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="6c47e-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c47e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c47e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c47e-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6c47e-125">The resource group name</span></span>

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

### <span data-ttu-id="6c47e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c47e-126">-ResourceId</span></span>
<span data-ttu-id="6c47e-127">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="6c47e-127">The agent resource id</span></span>

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

### <span data-ttu-id="6c47e-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6c47e-128">-ServerName</span></span>
<span data-ttu-id="6c47e-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="6c47e-129">The server name</span></span>

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

### <span data-ttu-id="6c47e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c47e-130">-Confirm</span></span>
<span data-ttu-id="6c47e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c47e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c47e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c47e-132">-WhatIf</span></span>
<span data-ttu-id="6c47e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c47e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c47e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c47e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c47e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c47e-135">CommonParameters</span></span>
<span data-ttu-id="6c47e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c47e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c47e-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c47e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c47e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c47e-138">INPUTS</span></span>

### <span data-ttu-id="6c47e-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6c47e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6c47e-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c47e-140">OUTPUTS</span></span>

### <span data-ttu-id="6c47e-141">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6c47e-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6c47e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c47e-142">NOTES</span></span>

## <span data-ttu-id="6c47e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c47e-143">RELATED LINKS</span></span>
