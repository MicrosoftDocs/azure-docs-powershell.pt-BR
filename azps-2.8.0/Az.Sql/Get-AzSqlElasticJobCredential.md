---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 13878e7ca0ea4ed0b03734f0395c9f819e04d7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773633"
---
# <span data-ttu-id="3caeb-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="3caeb-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="3caeb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3caeb-102">SYNOPSIS</span></span>
<span data-ttu-id="3caeb-103">Obtém uma ou mais credenciais</span><span class="sxs-lookup"><span data-stu-id="3caeb-103">Gets one or more credentials</span></span>

## <span data-ttu-id="3caeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3caeb-104">SYNTAX</span></span>

### <span data-ttu-id="3caeb-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="3caeb-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3caeb-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3caeb-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3caeb-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="3caeb-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3caeb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3caeb-108">DESCRIPTION</span></span>
<span data-ttu-id="3caeb-109">O cmdlet Get-AzSqlElasticJobCredential Obtém uma ou mais credenciais do trabalho</span><span class="sxs-lookup"><span data-stu-id="3caeb-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="3caeb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3caeb-110">EXAMPLES</span></span>

### <span data-ttu-id="3caeb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3caeb-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="3caeb-112">Obtém uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="3caeb-112">Gets a job credential</span></span>

## <span data-ttu-id="3caeb-113">OS</span><span class="sxs-lookup"><span data-stu-id="3caeb-113">PARAMETERS</span></span>

### <span data-ttu-id="3caeb-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3caeb-114">-AgentName</span></span>
<span data-ttu-id="3caeb-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="3caeb-115">The agent name</span></span>

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

### <span data-ttu-id="3caeb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3caeb-116">-DefaultProfile</span></span>
<span data-ttu-id="3caeb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3caeb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3caeb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3caeb-118">-Name</span></span>
<span data-ttu-id="3caeb-119">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="3caeb-119">The job credential name</span></span>

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

### <span data-ttu-id="3caeb-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3caeb-120">-ParentObject</span></span>
<span data-ttu-id="3caeb-121">O objeto agente</span><span class="sxs-lookup"><span data-stu-id="3caeb-121">The agent object</span></span>

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

### <span data-ttu-id="3caeb-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3caeb-122">-ParentResourceId</span></span>
<span data-ttu-id="3caeb-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="3caeb-123">The agent resource id</span></span>

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

### <span data-ttu-id="3caeb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3caeb-124">-ResourceGroupName</span></span>
<span data-ttu-id="3caeb-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3caeb-125">The resource group name</span></span>

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

### <span data-ttu-id="3caeb-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3caeb-126">-ServerName</span></span>
<span data-ttu-id="3caeb-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="3caeb-127">The server name</span></span>

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

### <span data-ttu-id="3caeb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caeb-128">CommonParameters</span></span>
<span data-ttu-id="3caeb-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3caeb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caeb-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3caeb-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caeb-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3caeb-131">INPUTS</span></span>

### <span data-ttu-id="3caeb-132">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3caeb-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3caeb-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3caeb-133">OUTPUTS</span></span>

### <span data-ttu-id="3caeb-134">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="3caeb-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="3caeb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3caeb-135">NOTES</span></span>

## <span data-ttu-id="3caeb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3caeb-136">RELATED LINKS</span></span>
