---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112551"
---
# <span data-ttu-id="266b7-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="266b7-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="266b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="266b7-102">SYNOPSIS</span></span>
<span data-ttu-id="266b7-103">Obtém um ou mais grupos de destino de trabalho</span><span class="sxs-lookup"><span data-stu-id="266b7-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="266b7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="266b7-104">SYNTAX</span></span>

### <span data-ttu-id="266b7-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="266b7-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="266b7-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="266b7-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="266b7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="266b7-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="266b7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="266b7-108">DESCRIPTION</span></span>
<span data-ttu-id="266b7-109">O Get-AzSqlElasticJobTargetGroup cmdlet obtém um grupo de destino e seus destinos</span><span class="sxs-lookup"><span data-stu-id="266b7-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="266b7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="266b7-110">EXAMPLES</span></span>

### <span data-ttu-id="266b7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="266b7-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="266b7-112">Obtém um grupo de destino e seus destinos</span><span class="sxs-lookup"><span data-stu-id="266b7-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="266b7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="266b7-113">PARAMETERS</span></span>

### <span data-ttu-id="266b7-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="266b7-114">-AgentName</span></span>
<span data-ttu-id="266b7-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="266b7-115">The agent name</span></span>

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

### <span data-ttu-id="266b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266b7-116">-DefaultProfile</span></span>
<span data-ttu-id="266b7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="266b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="266b7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="266b7-118">-Name</span></span>
<span data-ttu-id="266b7-119">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="266b7-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="266b7-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="266b7-120">-ParentObject</span></span>
<span data-ttu-id="266b7-121">O objeto do agente</span><span class="sxs-lookup"><span data-stu-id="266b7-121">The agent object</span></span>

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

### <span data-ttu-id="266b7-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="266b7-122">-ParentResourceId</span></span>
<span data-ttu-id="266b7-123">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="266b7-123">The agent resource id</span></span>

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

### <span data-ttu-id="266b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="266b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="266b7-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="266b7-125">The resource group name</span></span>

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

### <span data-ttu-id="266b7-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="266b7-126">-ServerName</span></span>
<span data-ttu-id="266b7-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="266b7-127">The server name</span></span>

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

### <span data-ttu-id="266b7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266b7-128">CommonParameters</span></span>
<span data-ttu-id="266b7-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="266b7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266b7-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="266b7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266b7-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="266b7-131">INPUTS</span></span>

### <span data-ttu-id="266b7-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="266b7-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="266b7-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="266b7-133">OUTPUTS</span></span>

### <span data-ttu-id="266b7-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="266b7-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="266b7-135">Notas</span><span class="sxs-lookup"><span data-stu-id="266b7-135">NOTES</span></span>

## <span data-ttu-id="266b7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="266b7-136">RELATED LINKS</span></span>
