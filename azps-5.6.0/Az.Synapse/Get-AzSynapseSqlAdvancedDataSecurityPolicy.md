---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 47800968fec9a12255bae01499618f9928416648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901540"
---
# <span data-ttu-id="80ce7-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="80ce7-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="80ce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="80ce7-103">Obtém a política avançada de Segurança de Dados de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="80ce7-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="80ce7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80ce7-104">SYNTAX</span></span>

### <span data-ttu-id="80ce7-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="80ce7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80ce7-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80ce7-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80ce7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80ce7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80ce7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80ce7-108">DESCRIPTION</span></span>
<span data-ttu-id="80ce7-109">O cmdlet **Get-AzSynapseSqlAdvancedDataSecurityPolicy** recupera a política de Segurança de Dados Avançada de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="80ce7-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="80ce7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80ce7-110">EXAMPLES</span></span>

### <span data-ttu-id="80ce7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80ce7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="80ce7-112">Este comando obtém a Segurança Avançada de Dados no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="80ce7-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="80ce7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="80ce7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="80ce7-114">Este comando obtém a Segurança Avançada de Dados no espaço de trabalho chamado ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="80ce7-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="80ce7-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80ce7-115">PARAMETERS</span></span>

### <span data-ttu-id="80ce7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ce7-116">-DefaultProfile</span></span>
<span data-ttu-id="80ce7-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80ce7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80ce7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80ce7-118">-InputObject</span></span>
<span data-ttu-id="80ce7-119">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="80ce7-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80ce7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ce7-120">-ResourceGroupName</span></span>
<span data-ttu-id="80ce7-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="80ce7-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ce7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80ce7-122">-ResourceId</span></span>
<span data-ttu-id="80ce7-123">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="80ce7-123">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ce7-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="80ce7-124">-WorkspaceName</span></span>
<span data-ttu-id="80ce7-125">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="80ce7-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ce7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ce7-126">CommonParameters</span></span>
<span data-ttu-id="80ce7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ce7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ce7-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80ce7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ce7-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80ce7-129">INPUTS</span></span>

### <span data-ttu-id="80ce7-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="80ce7-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="80ce7-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80ce7-131">OUTPUTS</span></span>

### <span data-ttu-id="80ce7-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="80ce7-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="80ce7-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="80ce7-133">NOTES</span></span>

## <span data-ttu-id="80ce7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80ce7-134">RELATED LINKS</span></span>
