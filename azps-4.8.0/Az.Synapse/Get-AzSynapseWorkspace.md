---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111218"
---
# <span data-ttu-id="b0d37-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b0d37-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="b0d37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0d37-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d37-103">Obtém um espaço de trabalho de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0d37-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="b0d37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0d37-104">SYNTAX</span></span>

### <span data-ttu-id="b0d37-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0d37-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0d37-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0d37-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d37-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0d37-107">DESCRIPTION</span></span>
<span data-ttu-id="b0d37-108">O cmdlet **Get-AzSynapseWorkspace** Obtém informações sobre um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0d37-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="b0d37-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0d37-109">EXAMPLES</span></span>

### <span data-ttu-id="b0d37-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b0d37-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="b0d37-111">Esse comando obtém todos os espaços de trabalho de análise do Azure Synapse sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b0d37-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="b0d37-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b0d37-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="b0d37-113">Esse comando obtém todos os espaços de trabalho de análise do Azure Synapse sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b0d37-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="b0d37-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b0d37-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="b0d37-115">Esse comando obtém o espaço de trabalho de análise do Azure Synapse com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="b0d37-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="b0d37-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="b0d37-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="b0d37-117">Esse comando obtém o espaço de trabalho de análise do Azure Synapse com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="b0d37-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="b0d37-118">OS</span><span class="sxs-lookup"><span data-stu-id="b0d37-118">PARAMETERS</span></span>

### <span data-ttu-id="b0d37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d37-119">-DefaultProfile</span></span>
<span data-ttu-id="b0d37-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d37-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d37-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0d37-121">-Name</span></span>
<span data-ttu-id="b0d37-122">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0d37-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b0d37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d37-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0d37-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0d37-124">Resource group name.</span></span>

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

### <span data-ttu-id="b0d37-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0d37-125">-ResourceId</span></span>
<span data-ttu-id="b0d37-126">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0d37-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="b0d37-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d37-127">CommonParameters</span></span>
<span data-ttu-id="b0d37-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d37-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d37-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0d37-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d37-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0d37-130">INPUTS</span></span>

### <span data-ttu-id="b0d37-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b0d37-131">None</span></span>

## <span data-ttu-id="b0d37-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0d37-132">OUTPUTS</span></span>

### <span data-ttu-id="b0d37-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b0d37-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b0d37-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0d37-134">NOTES</span></span>

## <span data-ttu-id="b0d37-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0d37-135">RELATED LINKS</span></span>
