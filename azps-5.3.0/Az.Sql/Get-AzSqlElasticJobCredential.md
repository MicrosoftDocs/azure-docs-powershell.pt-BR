---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271373"
---
# <span data-ttu-id="3d4fe-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="3d4fe-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="3d4fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4fe-103">Obtém uma ou mais credenciais</span><span class="sxs-lookup"><span data-stu-id="3d4fe-103">Gets one or more credentials</span></span>

## <span data-ttu-id="3d4fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d4fe-104">SYNTAX</span></span>

### <span data-ttu-id="3d4fe-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="3d4fe-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d4fe-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3d4fe-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d4fe-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="3d4fe-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d4fe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d4fe-108">DESCRIPTION</span></span>
<span data-ttu-id="3d4fe-109">O cmdlet Get-AzSqlElasticJobCredential Obtém uma ou mais credenciais do trabalho</span><span class="sxs-lookup"><span data-stu-id="3d4fe-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="3d4fe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d4fe-110">EXAMPLES</span></span>

### <span data-ttu-id="3d4fe-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d4fe-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="3d4fe-112">Obtém uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="3d4fe-112">Gets a job credential</span></span>

## <span data-ttu-id="3d4fe-113">OS</span><span class="sxs-lookup"><span data-stu-id="3d4fe-113">PARAMETERS</span></span>

### <span data-ttu-id="3d4fe-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3d4fe-114">-AgentName</span></span>
<span data-ttu-id="3d4fe-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="3d4fe-115">The agent name</span></span>

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

### <span data-ttu-id="3d4fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4fe-116">-DefaultProfile</span></span>
<span data-ttu-id="3d4fe-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d4fe-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d4fe-118">-Name</span></span>
<span data-ttu-id="3d4fe-119">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="3d4fe-119">The job credential name</span></span>

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

### <span data-ttu-id="3d4fe-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3d4fe-120">-ParentObject</span></span>
<span data-ttu-id="3d4fe-121">O objeto agente</span><span class="sxs-lookup"><span data-stu-id="3d4fe-121">The agent object</span></span>

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

### <span data-ttu-id="3d4fe-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3d4fe-122">-ParentResourceId</span></span>
<span data-ttu-id="3d4fe-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="3d4fe-123">The agent resource id</span></span>

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

### <span data-ttu-id="3d4fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d4fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d4fe-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3d4fe-125">The resource group name</span></span>

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

### <span data-ttu-id="3d4fe-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3d4fe-126">-ServerName</span></span>
<span data-ttu-id="3d4fe-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="3d4fe-127">The server name</span></span>

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

### <span data-ttu-id="3d4fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4fe-128">CommonParameters</span></span>
<span data-ttu-id="3d4fe-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d4fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4fe-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d4fe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4fe-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d4fe-131">INPUTS</span></span>

### <span data-ttu-id="3d4fe-132">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3d4fe-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3d4fe-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d4fe-133">OUTPUTS</span></span>

### <span data-ttu-id="3d4fe-134">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="3d4fe-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="3d4fe-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d4fe-135">NOTES</span></span>

## <span data-ttu-id="3d4fe-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d4fe-136">RELATED LINKS</span></span>
