---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943192"
---
# <span data-ttu-id="229f0-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="229f0-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="229f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="229f0-102">SYNOPSIS</span></span>
<span data-ttu-id="229f0-103">Remove a credencial de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="229f0-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="229f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="229f0-104">SYNTAX</span></span>

### <span data-ttu-id="229f0-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="229f0-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229f0-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="229f0-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229f0-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="229f0-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="229f0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="229f0-108">DESCRIPTION</span></span>
<span data-ttu-id="229f0-109">O cmdlet Remove-AzSqlElasticJobCredential remove uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="229f0-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="229f0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="229f0-110">EXAMPLES</span></span>

### <span data-ttu-id="229f0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="229f0-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="229f0-112">Remove uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="229f0-112">Removes a job credential</span></span>

## <span data-ttu-id="229f0-113">OS</span><span class="sxs-lookup"><span data-stu-id="229f0-113">PARAMETERS</span></span>

### <span data-ttu-id="229f0-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="229f0-114">-AgentName</span></span>
<span data-ttu-id="229f0-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="229f0-115">The agent name</span></span>

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

### <span data-ttu-id="229f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229f0-116">-DefaultProfile</span></span>
<span data-ttu-id="229f0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="229f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="229f0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="229f0-118">-InputObject</span></span>
<span data-ttu-id="229f0-119">O objeto de credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="229f0-119">The job credential object</span></span>

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

### <span data-ttu-id="229f0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="229f0-120">-Name</span></span>
<span data-ttu-id="229f0-121">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="229f0-121">The job credential name</span></span>

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

### <span data-ttu-id="229f0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="229f0-122">-ResourceGroupName</span></span>
<span data-ttu-id="229f0-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="229f0-123">The resource group name</span></span>

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

### <span data-ttu-id="229f0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="229f0-124">-ResourceId</span></span>
<span data-ttu-id="229f0-125">A ID do recurso de credenciais do trabalho</span><span class="sxs-lookup"><span data-stu-id="229f0-125">The job credential resource id</span></span>

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

### <span data-ttu-id="229f0-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="229f0-126">-ServerName</span></span>
<span data-ttu-id="229f0-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="229f0-127">The server name</span></span>

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

### <span data-ttu-id="229f0-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="229f0-128">-Confirm</span></span>
<span data-ttu-id="229f0-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="229f0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="229f0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="229f0-130">-WhatIf</span></span>
<span data-ttu-id="229f0-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="229f0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="229f0-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="229f0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="229f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229f0-133">CommonParameters</span></span>
<span data-ttu-id="229f0-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229f0-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="229f0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229f0-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="229f0-136">INPUTS</span></span>

### <span data-ttu-id="229f0-137">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="229f0-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="229f0-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="229f0-138">OUTPUTS</span></span>

### <span data-ttu-id="229f0-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="229f0-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="229f0-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="229f0-140">NOTES</span></span>

## <span data-ttu-id="229f0-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="229f0-141">RELATED LINKS</span></span>
