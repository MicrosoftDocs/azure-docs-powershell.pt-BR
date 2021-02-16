---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118606"
---
# <span data-ttu-id="de86c-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="de86c-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="de86c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de86c-102">SYNOPSIS</span></span>
<span data-ttu-id="de86c-103">Cria um novo agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="de86c-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="de86c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de86c-104">SYNTAX</span></span>

### <span data-ttu-id="de86c-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de86c-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de86c-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="de86c-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de86c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="de86c-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de86c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="de86c-108">DESCRIPTION</span></span>
<span data-ttu-id="de86c-109">O New-AzSqlElasticJobAgent cmdlet cria um novo agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="de86c-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="de86c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de86c-110">EXAMPLES</span></span>

### <span data-ttu-id="de86c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de86c-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="de86c-112">Cria um novo agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="de86c-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="de86c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de86c-113">PARAMETERS</span></span>

### <span data-ttu-id="de86c-114">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="de86c-114">-DatabaseName</span></span>
<span data-ttu-id="de86c-115">O nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="de86c-115">The database name</span></span>

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

### <span data-ttu-id="de86c-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="de86c-116">-DatabaseObject</span></span>
<span data-ttu-id="de86c-117">O Objeto de Banco de Dados de Controle de Agente</span><span class="sxs-lookup"><span data-stu-id="de86c-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="de86c-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="de86c-118">-DatabaseResourceId</span></span>
<span data-ttu-id="de86c-119">A ID do Recurso de Banco de Dados de Controle do Agente</span><span class="sxs-lookup"><span data-stu-id="de86c-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="de86c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de86c-120">-DefaultProfile</span></span>
<span data-ttu-id="de86c-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de86c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de86c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="de86c-122">-Name</span></span>
<span data-ttu-id="de86c-123">O Nome do Agente</span><span class="sxs-lookup"><span data-stu-id="de86c-123">The Agent Name</span></span>

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

### <span data-ttu-id="de86c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de86c-124">-ResourceGroupName</span></span>
<span data-ttu-id="de86c-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="de86c-125">The resource group name</span></span>

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

### <span data-ttu-id="de86c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="de86c-126">-ServerName</span></span>
<span data-ttu-id="de86c-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="de86c-127">The server name</span></span>

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

### <span data-ttu-id="de86c-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="de86c-128">-Tag</span></span>
<span data-ttu-id="de86c-129">As Marcas de Agente</span><span class="sxs-lookup"><span data-stu-id="de86c-129">The Agent Tags</span></span>

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

### <span data-ttu-id="de86c-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="de86c-130">-Confirm</span></span>
<span data-ttu-id="de86c-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de86c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de86c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de86c-132">-WhatIf</span></span>
<span data-ttu-id="de86c-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="de86c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de86c-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de86c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de86c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de86c-135">CommonParameters</span></span>
<span data-ttu-id="de86c-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de86c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de86c-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de86c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de86c-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="de86c-138">INPUTS</span></span>

### <span data-ttu-id="de86c-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="de86c-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="de86c-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="de86c-140">OUTPUTS</span></span>

### <span data-ttu-id="de86c-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="de86c-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="de86c-142">Notas</span><span class="sxs-lookup"><span data-stu-id="de86c-142">NOTES</span></span>

## <span data-ttu-id="de86c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de86c-143">RELATED LINKS</span></span>
