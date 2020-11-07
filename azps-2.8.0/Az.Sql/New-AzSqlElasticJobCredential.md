---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: d6b39aa8a2817afee952c8126ede6e07a73a05b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773570"
---
# <span data-ttu-id="d9c73-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="d9c73-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="d9c73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9c73-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c73-103">Cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="d9c73-103">Creates a new job credential</span></span>

## <span data-ttu-id="d9c73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9c73-104">SYNTAX</span></span>

### <span data-ttu-id="d9c73-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9c73-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c73-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9c73-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c73-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="d9c73-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c73-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9c73-108">DESCRIPTION</span></span>
<span data-ttu-id="d9c73-109">O cmdlet New-AzSqlElasticJobCredential cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="d9c73-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="d9c73-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9c73-110">EXAMPLES</span></span>

### <span data-ttu-id="d9c73-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d9c73-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="d9c73-112">Cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="d9c73-112">Creates a new job credential</span></span>

## <span data-ttu-id="d9c73-113">OS</span><span class="sxs-lookup"><span data-stu-id="d9c73-113">PARAMETERS</span></span>

### <span data-ttu-id="d9c73-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d9c73-114">-AgentName</span></span>
<span data-ttu-id="d9c73-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="d9c73-115">The agent name</span></span>

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

### <span data-ttu-id="d9c73-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="d9c73-116">-Credential</span></span>
<span data-ttu-id="d9c73-117">A credencial</span><span class="sxs-lookup"><span data-stu-id="d9c73-117">The credential</span></span>

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

### <span data-ttu-id="d9c73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c73-118">-DefaultProfile</span></span>
<span data-ttu-id="d9c73-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c73-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9c73-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9c73-120">-Name</span></span>
<span data-ttu-id="d9c73-121">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="d9c73-121">The job credential name</span></span>

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

### <span data-ttu-id="d9c73-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d9c73-122">-ParentObject</span></span>
<span data-ttu-id="d9c73-123">O objeto agente</span><span class="sxs-lookup"><span data-stu-id="d9c73-123">The agent object</span></span>

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

### <span data-ttu-id="d9c73-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c73-124">-ParentResourceId</span></span>
<span data-ttu-id="d9c73-125">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="d9c73-125">The agent resource id</span></span>

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

### <span data-ttu-id="d9c73-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c73-126">-ResourceGroupName</span></span>
<span data-ttu-id="d9c73-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d9c73-127">The resource group name</span></span>

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

### <span data-ttu-id="d9c73-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d9c73-128">-ServerName</span></span>
<span data-ttu-id="d9c73-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="d9c73-129">The server name</span></span>

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

### <span data-ttu-id="d9c73-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9c73-130">-Confirm</span></span>
<span data-ttu-id="d9c73-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c73-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c73-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c73-132">-WhatIf</span></span>
<span data-ttu-id="d9c73-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9c73-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c73-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9c73-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c73-135">CommonParameters</span></span>
<span data-ttu-id="d9c73-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c73-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9c73-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c73-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9c73-138">INPUTS</span></span>

### <span data-ttu-id="d9c73-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="d9c73-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="d9c73-140">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d9c73-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d9c73-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9c73-141">OUTPUTS</span></span>

### <span data-ttu-id="d9c73-142">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="d9c73-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="d9c73-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9c73-143">NOTES</span></span>

## <span data-ttu-id="d9c73-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9c73-144">RELATED LINKS</span></span>