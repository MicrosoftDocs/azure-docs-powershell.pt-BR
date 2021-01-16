---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272426"
---
# <span data-ttu-id="ad3e8-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="ad3e8-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="ad3e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3e8-103">Obtém a política de segurança de dados avançada de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="ad3e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad3e8-104">SYNTAX</span></span>

### <span data-ttu-id="ad3e8-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ad3e8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad3e8-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad3e8-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad3e8-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad3e8-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad3e8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad3e8-108">DESCRIPTION</span></span>
<span data-ttu-id="ad3e8-109">O cmdlet **Get-AzSynapseSqlAdvancedDataSecurityPolicy** recupera a política de segurança de dados avançada de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="ad3e8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad3e8-110">EXAMPLES</span></span>

### <span data-ttu-id="ad3e8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ad3e8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ad3e8-112">Esse comando obtém a segurança avançada de dados no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ad3e8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ad3e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="ad3e8-114">Esse comando obtém a segurança avançada de dados no espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ad3e8-115">OS</span><span class="sxs-lookup"><span data-stu-id="ad3e8-115">PARAMETERS</span></span>

### <span data-ttu-id="ad3e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3e8-116">-DefaultProfile</span></span>
<span data-ttu-id="ad3e8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad3e8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad3e8-118">-InputObject</span></span>
<span data-ttu-id="ad3e8-119">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ad3e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="ad3e8-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-121">Resource group name.</span></span>

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

### <span data-ttu-id="ad3e8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad3e8-122">-ResourceId</span></span>
<span data-ttu-id="ad3e8-123">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="ad3e8-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ad3e8-124">-WorkspaceName</span></span>
<span data-ttu-id="ad3e8-125">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ad3e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3e8-126">CommonParameters</span></span>
<span data-ttu-id="ad3e8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3e8-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad3e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3e8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad3e8-129">INPUTS</span></span>

### <span data-ttu-id="ad3e8-130">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ad3e8-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ad3e8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad3e8-131">OUTPUTS</span></span>

### <span data-ttu-id="ad3e8-132">Microsoft. Azure. Commands. Synapse. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="ad3e8-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="ad3e8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad3e8-133">NOTES</span></span>

## <span data-ttu-id="ad3e8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad3e8-134">RELATED LINKS</span></span>
