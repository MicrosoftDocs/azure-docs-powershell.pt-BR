---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 466df2e5be2c9193cce49cf9b06a5f8ff0d10e94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901398"
---
# <span data-ttu-id="a352f-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="a352f-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="a352f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a352f-102">SYNOPSIS</span></span>
<span data-ttu-id="a352f-103">Obtém uma ou mais credenciais</span><span class="sxs-lookup"><span data-stu-id="a352f-103">Gets one or more credentials</span></span>

## <span data-ttu-id="a352f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a352f-104">SYNTAX</span></span>

### <span data-ttu-id="a352f-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a352f-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a352f-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a352f-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a352f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a352f-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a352f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a352f-108">DESCRIPTION</span></span>
<span data-ttu-id="a352f-109">O Get-AzSqlElasticJobCredential cmdlet obtém uma ou mais credenciais de trabalho</span><span class="sxs-lookup"><span data-stu-id="a352f-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="a352f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a352f-110">EXAMPLES</span></span>

### <span data-ttu-id="a352f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a352f-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="a352f-112">Obtém uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="a352f-112">Gets a job credential</span></span>

## <span data-ttu-id="a352f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a352f-113">PARAMETERS</span></span>

### <span data-ttu-id="a352f-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a352f-114">-AgentName</span></span>
<span data-ttu-id="a352f-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="a352f-115">The agent name</span></span>

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

### <span data-ttu-id="a352f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a352f-116">-DefaultProfile</span></span>
<span data-ttu-id="a352f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a352f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a352f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a352f-118">-Name</span></span>
<span data-ttu-id="a352f-119">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="a352f-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a352f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a352f-120">-ParentObject</span></span>
<span data-ttu-id="a352f-121">O objeto agent</span><span class="sxs-lookup"><span data-stu-id="a352f-121">The agent object</span></span>

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

### <span data-ttu-id="a352f-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a352f-122">-ParentResourceId</span></span>
<span data-ttu-id="a352f-123">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="a352f-123">The agent resource id</span></span>

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

### <span data-ttu-id="a352f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a352f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a352f-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a352f-125">The resource group name</span></span>

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

### <span data-ttu-id="a352f-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a352f-126">-ServerName</span></span>
<span data-ttu-id="a352f-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="a352f-127">The server name</span></span>

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

### <span data-ttu-id="a352f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a352f-128">CommonParameters</span></span>
<span data-ttu-id="a352f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a352f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a352f-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a352f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a352f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a352f-131">INPUTS</span></span>

### <span data-ttu-id="a352f-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a352f-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a352f-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a352f-133">OUTPUTS</span></span>

### <span data-ttu-id="a352f-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="a352f-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="a352f-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="a352f-135">NOTES</span></span>

## <span data-ttu-id="a352f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a352f-136">RELATED LINKS</span></span>
