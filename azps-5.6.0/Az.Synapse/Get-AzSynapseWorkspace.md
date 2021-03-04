---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: 25107456afbf85aa41dd0be600a20f7a5fcbb640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887649"
---
# <span data-ttu-id="0eae8-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0eae8-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="0eae8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eae8-102">SYNOPSIS</span></span>
<span data-ttu-id="0eae8-103">Obtém um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0eae8-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0eae8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0eae8-104">SYNTAX</span></span>

### <span data-ttu-id="0eae8-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0eae8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eae8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eae8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eae8-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0eae8-107">DESCRIPTION</span></span>
<span data-ttu-id="0eae8-108">O cmdlet **Get-AzSynapseWorkspace** obtém informações sobre um espaço de trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0eae8-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0eae8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0eae8-109">EXAMPLES</span></span>

### <span data-ttu-id="0eae8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0eae8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="0eae8-111">Este comando obtém todos os espaços de trabalho do Azure Synapse Analytics na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0eae8-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="0eae8-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0eae8-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="0eae8-113">Este comando obtém todos os espaços de trabalho do Azure Synapse Analytics na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0eae8-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="0eae8-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0eae8-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="0eae8-115">Este comando obtém o espaço de trabalho do Azure Synapse Analytics com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="0eae8-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="0eae8-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="0eae8-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="0eae8-117">Este comando obtém o espaço de trabalho do Azure Synapse Analytics com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="0eae8-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="0eae8-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0eae8-118">PARAMETERS</span></span>

### <span data-ttu-id="0eae8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eae8-119">-DefaultProfile</span></span>
<span data-ttu-id="0eae8-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0eae8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eae8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0eae8-121">-Name</span></span>
<span data-ttu-id="0eae8-122">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="0eae8-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eae8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eae8-123">-ResourceGroupName</span></span>
<span data-ttu-id="0eae8-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0eae8-124">Resource group name.</span></span>

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

### <span data-ttu-id="0eae8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eae8-125">-ResourceId</span></span>
<span data-ttu-id="0eae8-126">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="0eae8-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="0eae8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eae8-127">CommonParameters</span></span>
<span data-ttu-id="0eae8-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eae8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eae8-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eae8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eae8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0eae8-130">INPUTS</span></span>

### <span data-ttu-id="0eae8-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0eae8-131">None</span></span>

## <span data-ttu-id="0eae8-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0eae8-132">OUTPUTS</span></span>

### <span data-ttu-id="0eae8-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0eae8-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0eae8-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="0eae8-134">NOTES</span></span>

## <span data-ttu-id="0eae8-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0eae8-135">RELATED LINKS</span></span>
