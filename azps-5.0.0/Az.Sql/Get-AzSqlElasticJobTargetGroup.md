---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280442"
---
# <span data-ttu-id="91325-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="91325-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="91325-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91325-102">SYNOPSIS</span></span>
<span data-ttu-id="91325-103">Obtém um ou mais grupos de alvos de trabalho</span><span class="sxs-lookup"><span data-stu-id="91325-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="91325-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91325-104">SYNTAX</span></span>

### <span data-ttu-id="91325-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="91325-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91325-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="91325-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91325-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="91325-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91325-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91325-108">DESCRIPTION</span></span>
<span data-ttu-id="91325-109">O cmdlet Get-AzSqlElasticJobTargetGroup Obtém um grupo de destino e é alvo</span><span class="sxs-lookup"><span data-stu-id="91325-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="91325-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91325-110">EXAMPLES</span></span>

### <span data-ttu-id="91325-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91325-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="91325-112">Obtém um grupo de destino e seus destinos</span><span class="sxs-lookup"><span data-stu-id="91325-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="91325-113">OS</span><span class="sxs-lookup"><span data-stu-id="91325-113">PARAMETERS</span></span>

### <span data-ttu-id="91325-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="91325-114">-AgentName</span></span>
<span data-ttu-id="91325-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="91325-115">The agent name</span></span>

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

### <span data-ttu-id="91325-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91325-116">-DefaultProfile</span></span>
<span data-ttu-id="91325-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91325-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91325-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="91325-118">-Name</span></span>
<span data-ttu-id="91325-119">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="91325-119">The target group name</span></span>

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

### <span data-ttu-id="91325-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="91325-120">-ParentObject</span></span>
<span data-ttu-id="91325-121">O objeto agente</span><span class="sxs-lookup"><span data-stu-id="91325-121">The agent object</span></span>

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

### <span data-ttu-id="91325-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="91325-122">-ParentResourceId</span></span>
<span data-ttu-id="91325-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="91325-123">The agent resource id</span></span>

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

### <span data-ttu-id="91325-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91325-124">-ResourceGroupName</span></span>
<span data-ttu-id="91325-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="91325-125">The resource group name</span></span>

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

### <span data-ttu-id="91325-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="91325-126">-ServerName</span></span>
<span data-ttu-id="91325-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="91325-127">The server name</span></span>

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

### <span data-ttu-id="91325-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91325-128">CommonParameters</span></span>
<span data-ttu-id="91325-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91325-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91325-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91325-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91325-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91325-131">INPUTS</span></span>

### <span data-ttu-id="91325-132">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="91325-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="91325-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91325-133">OUTPUTS</span></span>

### <span data-ttu-id="91325-134">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="91325-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="91325-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91325-135">NOTES</span></span>

## <span data-ttu-id="91325-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91325-136">RELATED LINKS</span></span>
