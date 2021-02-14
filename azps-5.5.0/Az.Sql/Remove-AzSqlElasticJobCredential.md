---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110924"
---
# <span data-ttu-id="ca35b-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="ca35b-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="ca35b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca35b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca35b-103">Remove a credencial de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="ca35b-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="ca35b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca35b-104">SYNTAX</span></span>

### <span data-ttu-id="ca35b-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca35b-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca35b-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="ca35b-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca35b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca35b-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca35b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca35b-108">DESCRIPTION</span></span>
<span data-ttu-id="ca35b-109">O Remove-AzSqlElasticJobCredential cmdlet remove uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="ca35b-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="ca35b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca35b-110">EXAMPLES</span></span>

### <span data-ttu-id="ca35b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca35b-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="ca35b-112">Remove uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="ca35b-112">Removes a job credential</span></span>

## <span data-ttu-id="ca35b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca35b-113">PARAMETERS</span></span>

### <span data-ttu-id="ca35b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ca35b-114">-AgentName</span></span>
<span data-ttu-id="ca35b-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="ca35b-115">The agent name</span></span>

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

### <span data-ttu-id="ca35b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca35b-116">-DefaultProfile</span></span>
<span data-ttu-id="ca35b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca35b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca35b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca35b-118">-InputObject</span></span>
<span data-ttu-id="ca35b-119">O objeto de credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="ca35b-119">The job credential object</span></span>

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

### <span data-ttu-id="ca35b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca35b-120">-Name</span></span>
<span data-ttu-id="ca35b-121">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="ca35b-121">The job credential name</span></span>

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

### <span data-ttu-id="ca35b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca35b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca35b-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ca35b-123">The resource group name</span></span>

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

### <span data-ttu-id="ca35b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca35b-124">-ResourceId</span></span>
<span data-ttu-id="ca35b-125">A ID do recurso de credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="ca35b-125">The job credential resource id</span></span>

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

### <span data-ttu-id="ca35b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca35b-126">-ServerName</span></span>
<span data-ttu-id="ca35b-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="ca35b-127">The server name</span></span>

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

### <span data-ttu-id="ca35b-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ca35b-128">-Confirm</span></span>
<span data-ttu-id="ca35b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca35b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca35b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca35b-130">-WhatIf</span></span>
<span data-ttu-id="ca35b-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ca35b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca35b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca35b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca35b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca35b-133">CommonParameters</span></span>
<span data-ttu-id="ca35b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca35b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca35b-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca35b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca35b-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca35b-136">INPUTS</span></span>

### <span data-ttu-id="ca35b-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="ca35b-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="ca35b-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca35b-138">OUTPUTS</span></span>

### <span data-ttu-id="ca35b-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="ca35b-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="ca35b-140">Notas</span><span class="sxs-lookup"><span data-stu-id="ca35b-140">NOTES</span></span>

## <span data-ttu-id="ca35b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca35b-141">RELATED LINKS</span></span>
