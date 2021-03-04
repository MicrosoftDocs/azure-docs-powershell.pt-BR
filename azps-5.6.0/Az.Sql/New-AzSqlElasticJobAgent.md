---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: ca23ba63e2f92fa14c97957a2b21b38d91e453ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889138"
---
# <span data-ttu-id="4fcaf-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="4fcaf-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="4fcaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fcaf-102">SYNOPSIS</span></span>
<span data-ttu-id="4fcaf-103">Cria um novo agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="4fcaf-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="4fcaf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4fcaf-104">SYNTAX</span></span>

### <span data-ttu-id="4fcaf-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4fcaf-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fcaf-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4fcaf-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fcaf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4fcaf-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fcaf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4fcaf-108">DESCRIPTION</span></span>
<span data-ttu-id="4fcaf-109">O New-AzSqlElasticJobAgent cmdlet cria um novo agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="4fcaf-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="4fcaf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fcaf-110">EXAMPLES</span></span>

### <span data-ttu-id="4fcaf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fcaf-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="4fcaf-112">Cria um novo agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="4fcaf-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="4fcaf-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4fcaf-113">PARAMETERS</span></span>

### <span data-ttu-id="4fcaf-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4fcaf-114">-DatabaseName</span></span>
<span data-ttu-id="4fcaf-115">O nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="4fcaf-115">The database name</span></span>

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

### <span data-ttu-id="4fcaf-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4fcaf-116">-DatabaseObject</span></span>
<span data-ttu-id="4fcaf-117">O objeto de banco de dados de controle do agente</span><span class="sxs-lookup"><span data-stu-id="4fcaf-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fcaf-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="4fcaf-118">-DatabaseResourceId</span></span>
<span data-ttu-id="4fcaf-119">A ID do Recurso do Banco de Dados de Controle do Agente</span><span class="sxs-lookup"><span data-stu-id="4fcaf-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="4fcaf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fcaf-120">-DefaultProfile</span></span>
<span data-ttu-id="4fcaf-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcaf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fcaf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4fcaf-122">-Name</span></span>
<span data-ttu-id="4fcaf-123">O Nome do Agente</span><span class="sxs-lookup"><span data-stu-id="4fcaf-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fcaf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fcaf-124">-ResourceGroupName</span></span>
<span data-ttu-id="4fcaf-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4fcaf-125">The resource group name</span></span>

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

### <span data-ttu-id="4fcaf-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4fcaf-126">-ServerName</span></span>
<span data-ttu-id="4fcaf-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="4fcaf-127">The server name</span></span>

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

### <span data-ttu-id="4fcaf-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="4fcaf-128">-Tag</span></span>
<span data-ttu-id="4fcaf-129">As Marcas de Agente</span><span class="sxs-lookup"><span data-stu-id="4fcaf-129">The Agent Tags</span></span>

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

### <span data-ttu-id="4fcaf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fcaf-130">-Confirm</span></span>
<span data-ttu-id="4fcaf-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fcaf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fcaf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fcaf-132">-WhatIf</span></span>
<span data-ttu-id="4fcaf-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4fcaf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fcaf-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fcaf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fcaf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fcaf-135">CommonParameters</span></span>
<span data-ttu-id="4fcaf-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fcaf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fcaf-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fcaf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fcaf-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fcaf-138">INPUTS</span></span>

### <span data-ttu-id="4fcaf-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4fcaf-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4fcaf-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4fcaf-140">OUTPUTS</span></span>

### <span data-ttu-id="4fcaf-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="4fcaf-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4fcaf-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="4fcaf-142">NOTES</span></span>

## <span data-ttu-id="4fcaf-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fcaf-143">RELATED LINKS</span></span>
