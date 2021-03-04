---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 9c0d7348a900690a49ebea96bc90c296c2d8e9a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889714"
---
# <span data-ttu-id="55262-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="55262-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="55262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55262-102">SYNOPSIS</span></span>
<span data-ttu-id="55262-103">Atualiza uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="55262-103">Updates a job credential</span></span>

## <span data-ttu-id="55262-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="55262-104">SYNTAX</span></span>

### <span data-ttu-id="55262-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55262-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55262-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="55262-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55262-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="55262-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55262-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="55262-108">DESCRIPTION</span></span>
<span data-ttu-id="55262-109">O Set-AzSqlElasticJobCredential cmdlet atualiza uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="55262-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="55262-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55262-110">EXAMPLES</span></span>

### <span data-ttu-id="55262-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55262-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="55262-112">Atualiza uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="55262-112">Updates a job credential</span></span>

## <span data-ttu-id="55262-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="55262-113">PARAMETERS</span></span>

### <span data-ttu-id="55262-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="55262-114">-AgentName</span></span>
<span data-ttu-id="55262-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="55262-115">The agent name</span></span>

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

### <span data-ttu-id="55262-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="55262-116">-Credential</span></span>
<span data-ttu-id="55262-117">A credencial</span><span class="sxs-lookup"><span data-stu-id="55262-117">The credential</span></span>

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

### <span data-ttu-id="55262-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55262-118">-DefaultProfile</span></span>
<span data-ttu-id="55262-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55262-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55262-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55262-120">-InputObject</span></span>
<span data-ttu-id="55262-121">O objeto de credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="55262-121">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55262-122">-Name</span><span class="sxs-lookup"><span data-stu-id="55262-122">-Name</span></span>
<span data-ttu-id="55262-123">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="55262-123">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55262-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55262-124">-ResourceGroupName</span></span>
<span data-ttu-id="55262-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="55262-125">The resource group name</span></span>

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

### <span data-ttu-id="55262-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55262-126">-ResourceId</span></span>
<span data-ttu-id="55262-127">A ID do recurso de credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="55262-127">The job credential resource id</span></span>

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

### <span data-ttu-id="55262-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55262-128">-ServerName</span></span>
<span data-ttu-id="55262-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="55262-129">The server name</span></span>

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

### <span data-ttu-id="55262-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55262-130">-Confirm</span></span>
<span data-ttu-id="55262-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55262-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55262-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55262-132">-WhatIf</span></span>
<span data-ttu-id="55262-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55262-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55262-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55262-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55262-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55262-135">CommonParameters</span></span>
<span data-ttu-id="55262-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55262-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55262-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55262-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55262-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55262-138">INPUTS</span></span>

### <span data-ttu-id="55262-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="55262-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="55262-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="55262-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="55262-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="55262-141">OUTPUTS</span></span>

### <span data-ttu-id="55262-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="55262-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="55262-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="55262-143">NOTES</span></span>

## <span data-ttu-id="55262-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55262-144">RELATED LINKS</span></span>
