---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944257"
---
# <span data-ttu-id="7c619-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="7c619-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="7c619-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c619-102">SYNOPSIS</span></span>
<span data-ttu-id="7c619-103">Cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="7c619-103">Creates a new job credential</span></span>

## <span data-ttu-id="7c619-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c619-104">SYNTAX</span></span>

### <span data-ttu-id="7c619-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="7c619-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c619-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c619-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c619-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="7c619-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c619-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c619-108">DESCRIPTION</span></span>
<span data-ttu-id="7c619-109">O cmdlet New-AzSqlElasticJobCredential cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="7c619-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="7c619-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c619-110">EXAMPLES</span></span>

### <span data-ttu-id="7c619-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c619-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="7c619-112">Cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="7c619-112">Creates a new job credential</span></span>

## <span data-ttu-id="7c619-113">OS</span><span class="sxs-lookup"><span data-stu-id="7c619-113">PARAMETERS</span></span>

### <span data-ttu-id="7c619-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7c619-114">-AgentName</span></span>
<span data-ttu-id="7c619-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="7c619-115">The agent name</span></span>

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

### <span data-ttu-id="7c619-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="7c619-116">-Credential</span></span>
<span data-ttu-id="7c619-117">A credencial</span><span class="sxs-lookup"><span data-stu-id="7c619-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c619-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c619-118">-DefaultProfile</span></span>
<span data-ttu-id="7c619-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c619-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c619-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c619-120">-Name</span></span>
<span data-ttu-id="7c619-121">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="7c619-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c619-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7c619-122">-ParentObject</span></span>
<span data-ttu-id="7c619-123">O objeto agente</span><span class="sxs-lookup"><span data-stu-id="7c619-123">The agent object</span></span>

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

### <span data-ttu-id="7c619-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7c619-124">-ParentResourceId</span></span>
<span data-ttu-id="7c619-125">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="7c619-125">The agent resource id</span></span>

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

### <span data-ttu-id="7c619-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c619-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c619-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7c619-127">The resource group name</span></span>

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

### <span data-ttu-id="7c619-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7c619-128">-ServerName</span></span>
<span data-ttu-id="7c619-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="7c619-129">The server name</span></span>

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

### <span data-ttu-id="7c619-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7c619-130">-Confirm</span></span>
<span data-ttu-id="7c619-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c619-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c619-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c619-132">-WhatIf</span></span>
<span data-ttu-id="7c619-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c619-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c619-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c619-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c619-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c619-135">CommonParameters</span></span>
<span data-ttu-id="7c619-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c619-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c619-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c619-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c619-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c619-138">INPUTS</span></span>

### <span data-ttu-id="7c619-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="7c619-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="7c619-140">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="7c619-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="7c619-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c619-141">OUTPUTS</span></span>

### <span data-ttu-id="7c619-142">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="7c619-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="7c619-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c619-143">NOTES</span></span>

## <span data-ttu-id="7c619-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c619-144">RELATED LINKS</span></span>
