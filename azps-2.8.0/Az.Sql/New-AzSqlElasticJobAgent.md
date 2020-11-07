---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: e4517f99c44a734902f2d75ec7d432ad73ad8038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773840"
---
# <span data-ttu-id="273f7-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="273f7-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="273f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="273f7-102">SYNOPSIS</span></span>
<span data-ttu-id="273f7-103">Cria um novo agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="273f7-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="273f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="273f7-104">SYNTAX</span></span>

### <span data-ttu-id="273f7-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="273f7-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="273f7-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="273f7-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="273f7-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="273f7-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="273f7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="273f7-108">DESCRIPTION</span></span>
<span data-ttu-id="273f7-109">O cmdlet New-AzSqlElasticJobAgent cria um novo agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="273f7-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="273f7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="273f7-110">EXAMPLES</span></span>

### <span data-ttu-id="273f7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="273f7-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="273f7-112">Cria um novo agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="273f7-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="273f7-113">OS</span><span class="sxs-lookup"><span data-stu-id="273f7-113">PARAMETERS</span></span>

### <span data-ttu-id="273f7-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="273f7-114">-DatabaseName</span></span>
<span data-ttu-id="273f7-115">O nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="273f7-115">The database name</span></span>

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

### <span data-ttu-id="273f7-116">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="273f7-116">-DatabaseObject</span></span>
<span data-ttu-id="273f7-117">O objeto de banco de dados controle de agente</span><span class="sxs-lookup"><span data-stu-id="273f7-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="273f7-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="273f7-118">-DatabaseResourceId</span></span>
<span data-ttu-id="273f7-119">A ID do recurso de banco de dados do controle de agente</span><span class="sxs-lookup"><span data-stu-id="273f7-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="273f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273f7-120">-DefaultProfile</span></span>
<span data-ttu-id="273f7-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="273f7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="273f7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="273f7-122">-Name</span></span>
<span data-ttu-id="273f7-123">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="273f7-123">The Agent Name</span></span>

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

### <span data-ttu-id="273f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="273f7-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="273f7-125">The resource group name</span></span>

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

### <span data-ttu-id="273f7-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="273f7-126">-ServerName</span></span>
<span data-ttu-id="273f7-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="273f7-127">The server name</span></span>

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

### <span data-ttu-id="273f7-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="273f7-128">-Tag</span></span>
<span data-ttu-id="273f7-129">As marcas do agente</span><span class="sxs-lookup"><span data-stu-id="273f7-129">The Agent Tags</span></span>

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

### <span data-ttu-id="273f7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="273f7-130">-Confirm</span></span>
<span data-ttu-id="273f7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="273f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="273f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="273f7-132">-WhatIf</span></span>
<span data-ttu-id="273f7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="273f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="273f7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="273f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="273f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273f7-135">CommonParameters</span></span>
<span data-ttu-id="273f7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="273f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273f7-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="273f7-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273f7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="273f7-138">INPUTS</span></span>

### <span data-ttu-id="273f7-139">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="273f7-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="273f7-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="273f7-140">OUTPUTS</span></span>

### <span data-ttu-id="273f7-141">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="273f7-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="273f7-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="273f7-142">NOTES</span></span>

## <span data-ttu-id="273f7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="273f7-143">RELATED LINKS</span></span>
