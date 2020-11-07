---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954562"
---
# <span data-ttu-id="64491-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="64491-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="64491-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64491-102">SYNOPSIS</span></span>
<span data-ttu-id="64491-103">Atualiza um agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="64491-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="64491-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64491-104">SYNTAX</span></span>

### <span data-ttu-id="64491-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="64491-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64491-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="64491-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64491-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="64491-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64491-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64491-108">DESCRIPTION</span></span>
<span data-ttu-id="64491-109">O cmdlet Set-AzSqlElasticJobAgent atualiza um agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="64491-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="64491-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64491-110">EXAMPLES</span></span>

### <span data-ttu-id="64491-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64491-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="64491-112">Atualiza um agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="64491-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="64491-113">OS</span><span class="sxs-lookup"><span data-stu-id="64491-113">PARAMETERS</span></span>

### <span data-ttu-id="64491-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64491-114">-DefaultProfile</span></span>
<span data-ttu-id="64491-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64491-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64491-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64491-116">-InputObject</span></span>
<span data-ttu-id="64491-117">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="64491-117">The agent input object</span></span>

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

### <span data-ttu-id="64491-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="64491-118">-Name</span></span>
<span data-ttu-id="64491-119">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="64491-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64491-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64491-120">-ResourceGroupName</span></span>
<span data-ttu-id="64491-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="64491-121">The resource group name</span></span>

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

### <span data-ttu-id="64491-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64491-122">-ResourceId</span></span>
<span data-ttu-id="64491-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="64491-123">The agent resource id</span></span>

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

### <span data-ttu-id="64491-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="64491-124">-ServerName</span></span>
<span data-ttu-id="64491-125">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="64491-125">The server name</span></span>

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

### <span data-ttu-id="64491-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="64491-126">-Tag</span></span>
<span data-ttu-id="64491-127">As marcas a serem associadas ao agente de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="64491-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64491-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64491-128">-Confirm</span></span>
<span data-ttu-id="64491-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64491-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64491-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64491-130">-WhatIf</span></span>
<span data-ttu-id="64491-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64491-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64491-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64491-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64491-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64491-133">CommonParameters</span></span>
<span data-ttu-id="64491-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64491-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64491-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64491-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64491-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64491-136">INPUTS</span></span>

### <span data-ttu-id="64491-137">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="64491-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="64491-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64491-138">OUTPUTS</span></span>

### <span data-ttu-id="64491-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="64491-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="64491-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64491-140">NOTES</span></span>

## <span data-ttu-id="64491-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64491-141">RELATED LINKS</span></span>
