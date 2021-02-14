---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115710"
---
# <span data-ttu-id="4518d-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="4518d-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="4518d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4518d-102">SYNOPSIS</span></span>
<span data-ttu-id="4518d-103">Atualiza um agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="4518d-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="4518d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4518d-104">SYNTAX</span></span>

### <span data-ttu-id="4518d-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4518d-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4518d-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="4518d-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4518d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4518d-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4518d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4518d-108">DESCRIPTION</span></span>
<span data-ttu-id="4518d-109">O Set-AzSqlElasticJobAgent cmdlet atualiza os agentes de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="4518d-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="4518d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4518d-110">EXAMPLES</span></span>

### <span data-ttu-id="4518d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4518d-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="4518d-112">Atualiza um agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="4518d-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="4518d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4518d-113">PARAMETERS</span></span>

### <span data-ttu-id="4518d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4518d-114">-DefaultProfile</span></span>
<span data-ttu-id="4518d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4518d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4518d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4518d-116">-InputObject</span></span>
<span data-ttu-id="4518d-117">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="4518d-117">The agent input object</span></span>

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

### <span data-ttu-id="4518d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4518d-118">-Name</span></span>
<span data-ttu-id="4518d-119">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="4518d-119">The agent name</span></span>

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

### <span data-ttu-id="4518d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4518d-120">-ResourceGroupName</span></span>
<span data-ttu-id="4518d-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4518d-121">The resource group name</span></span>

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

### <span data-ttu-id="4518d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4518d-122">-ResourceId</span></span>
<span data-ttu-id="4518d-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="4518d-123">The agent resource id</span></span>

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

### <span data-ttu-id="4518d-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4518d-124">-ServerName</span></span>
<span data-ttu-id="4518d-125">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="4518d-125">The server name</span></span>

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

### <span data-ttu-id="4518d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="4518d-126">-Tag</span></span>
<span data-ttu-id="4518d-127">As marcas a associar ao Agente de Banco de Dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="4518d-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="4518d-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4518d-128">-Confirm</span></span>
<span data-ttu-id="4518d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4518d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4518d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4518d-130">-WhatIf</span></span>
<span data-ttu-id="4518d-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4518d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4518d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4518d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4518d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4518d-133">CommonParameters</span></span>
<span data-ttu-id="4518d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4518d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4518d-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4518d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4518d-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="4518d-136">INPUTS</span></span>

### <span data-ttu-id="4518d-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="4518d-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4518d-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="4518d-138">OUTPUTS</span></span>

### <span data-ttu-id="4518d-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="4518d-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4518d-140">Notas</span><span class="sxs-lookup"><span data-stu-id="4518d-140">NOTES</span></span>

## <span data-ttu-id="4518d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4518d-141">RELATED LINKS</span></span>
