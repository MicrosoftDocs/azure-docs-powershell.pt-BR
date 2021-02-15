---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114474"
---
# <span data-ttu-id="0bfcf-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="0bfcf-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="0bfcf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bfcf-102">SYNOPSIS</span></span>
<span data-ttu-id="0bfcf-103">Cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="0bfcf-103">Creates a new job credential</span></span>

## <span data-ttu-id="0bfcf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bfcf-104">SYNTAX</span></span>

### <span data-ttu-id="0bfcf-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0bfcf-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bfcf-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="0bfcf-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bfcf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0bfcf-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bfcf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bfcf-108">DESCRIPTION</span></span>
<span data-ttu-id="0bfcf-109">O New-AzSqlElasticJobCredential cmdlet cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="0bfcf-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="0bfcf-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0bfcf-110">EXAMPLES</span></span>

### <span data-ttu-id="0bfcf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0bfcf-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="0bfcf-112">Cria uma nova credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="0bfcf-112">Creates a new job credential</span></span>

## <span data-ttu-id="0bfcf-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bfcf-113">PARAMETERS</span></span>

### <span data-ttu-id="0bfcf-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0bfcf-114">-AgentName</span></span>
<span data-ttu-id="0bfcf-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="0bfcf-115">The agent name</span></span>

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

### <span data-ttu-id="0bfcf-116">-Credencial</span><span class="sxs-lookup"><span data-stu-id="0bfcf-116">-Credential</span></span>
<span data-ttu-id="0bfcf-117">A credencial</span><span class="sxs-lookup"><span data-stu-id="0bfcf-117">The credential</span></span>

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

### <span data-ttu-id="0bfcf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bfcf-118">-DefaultProfile</span></span>
<span data-ttu-id="0bfcf-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bfcf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bfcf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bfcf-120">-Name</span></span>
<span data-ttu-id="0bfcf-121">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="0bfcf-121">The job credential name</span></span>

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

### <span data-ttu-id="0bfcf-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0bfcf-122">-ParentObject</span></span>
<span data-ttu-id="0bfcf-123">O objeto do agente</span><span class="sxs-lookup"><span data-stu-id="0bfcf-123">The agent object</span></span>

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

### <span data-ttu-id="0bfcf-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0bfcf-124">-ParentResourceId</span></span>
<span data-ttu-id="0bfcf-125">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="0bfcf-125">The agent resource id</span></span>

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

### <span data-ttu-id="0bfcf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bfcf-126">-ResourceGroupName</span></span>
<span data-ttu-id="0bfcf-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0bfcf-127">The resource group name</span></span>

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

### <span data-ttu-id="0bfcf-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0bfcf-128">-ServerName</span></span>
<span data-ttu-id="0bfcf-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="0bfcf-129">The server name</span></span>

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

### <span data-ttu-id="0bfcf-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0bfcf-130">-Confirm</span></span>
<span data-ttu-id="0bfcf-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bfcf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bfcf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bfcf-132">-WhatIf</span></span>
<span data-ttu-id="0bfcf-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0bfcf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bfcf-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0bfcf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bfcf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bfcf-135">CommonParameters</span></span>
<span data-ttu-id="0bfcf-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bfcf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bfcf-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bfcf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bfcf-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="0bfcf-138">INPUTS</span></span>

### <span data-ttu-id="0bfcf-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="0bfcf-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="0bfcf-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="0bfcf-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="0bfcf-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="0bfcf-141">OUTPUTS</span></span>

### <span data-ttu-id="0bfcf-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="0bfcf-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="0bfcf-143">Notas</span><span class="sxs-lookup"><span data-stu-id="0bfcf-143">NOTES</span></span>

## <span data-ttu-id="0bfcf-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bfcf-144">RELATED LINKS</span></span>
