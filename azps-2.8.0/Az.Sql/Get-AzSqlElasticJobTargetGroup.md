---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: fd2f8cc12faa1a08eb8f30743c88d5d3e44e48fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773725"
---
# <span data-ttu-id="61667-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="61667-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="61667-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61667-102">SYNOPSIS</span></span>
<span data-ttu-id="61667-103">Obtém um ou mais grupos de alvos de trabalho</span><span class="sxs-lookup"><span data-stu-id="61667-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="61667-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61667-104">SYNTAX</span></span>

### <span data-ttu-id="61667-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="61667-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61667-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="61667-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61667-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="61667-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61667-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61667-108">DESCRIPTION</span></span>
<span data-ttu-id="61667-109">O cmdlet Get-AzSqlElasticJobTargetGroup Obtém um grupo de destino e é alvo</span><span class="sxs-lookup"><span data-stu-id="61667-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="61667-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61667-110">EXAMPLES</span></span>

### <span data-ttu-id="61667-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61667-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="61667-112">Obtém um grupo de destino e seus destinos</span><span class="sxs-lookup"><span data-stu-id="61667-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="61667-113">OS</span><span class="sxs-lookup"><span data-stu-id="61667-113">PARAMETERS</span></span>

### <span data-ttu-id="61667-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="61667-114">-AgentName</span></span>
<span data-ttu-id="61667-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="61667-115">The agent name</span></span>

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

### <span data-ttu-id="61667-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61667-116">-DefaultProfile</span></span>
<span data-ttu-id="61667-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61667-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61667-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="61667-118">-Name</span></span>
<span data-ttu-id="61667-119">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="61667-119">The target group name</span></span>

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

### <span data-ttu-id="61667-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="61667-120">-ParentObject</span></span>
<span data-ttu-id="61667-121">O objeto agente</span><span class="sxs-lookup"><span data-stu-id="61667-121">The agent object</span></span>

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

### <span data-ttu-id="61667-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="61667-122">-ParentResourceId</span></span>
<span data-ttu-id="61667-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="61667-123">The agent resource id</span></span>

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

### <span data-ttu-id="61667-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61667-124">-ResourceGroupName</span></span>
<span data-ttu-id="61667-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="61667-125">The resource group name</span></span>

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

### <span data-ttu-id="61667-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="61667-126">-ServerName</span></span>
<span data-ttu-id="61667-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="61667-127">The server name</span></span>

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

### <span data-ttu-id="61667-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61667-128">CommonParameters</span></span>
<span data-ttu-id="61667-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61667-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61667-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61667-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61667-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61667-131">INPUTS</span></span>

### <span data-ttu-id="61667-132">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="61667-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="61667-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61667-133">OUTPUTS</span></span>

### <span data-ttu-id="61667-134">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="61667-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="61667-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61667-135">NOTES</span></span>

## <span data-ttu-id="61667-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61667-136">RELATED LINKS</span></span>
