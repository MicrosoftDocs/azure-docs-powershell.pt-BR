---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114368"
---
# <span data-ttu-id="24902-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="24902-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="24902-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24902-102">SYNOPSIS</span></span>
<span data-ttu-id="24902-103">Obtém um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="24902-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="24902-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24902-104">SYNTAX</span></span>

### <span data-ttu-id="24902-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24902-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24902-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24902-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24902-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="24902-107">DESCRIPTION</span></span>
<span data-ttu-id="24902-108">O cmdlet **Get-AzSynapseWorkspace** obtém informações sobre um espaço de trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="24902-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="24902-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24902-109">EXAMPLES</span></span>

### <span data-ttu-id="24902-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24902-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="24902-111">Esse comando obtém todos os espaços de trabalho do Azure Synapse Analytics sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="24902-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="24902-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="24902-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="24902-113">Esse comando obtém todos os espaços de trabalho do Azure Synapse Analytics sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="24902-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="24902-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="24902-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="24902-115">Esse comando obtém o espaço de trabalho do Azure Synapse Analytics com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="24902-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="24902-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="24902-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="24902-117">Esse comando obtém o espaço de trabalho do Azure Synapse Analytics com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="24902-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="24902-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24902-118">PARAMETERS</span></span>

### <span data-ttu-id="24902-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24902-119">-DefaultProfile</span></span>
<span data-ttu-id="24902-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24902-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24902-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="24902-121">-Name</span></span>
<span data-ttu-id="24902-122">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="24902-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="24902-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24902-123">-ResourceGroupName</span></span>
<span data-ttu-id="24902-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24902-124">Resource group name.</span></span>

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

### <span data-ttu-id="24902-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24902-125">-ResourceId</span></span>
<span data-ttu-id="24902-126">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="24902-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="24902-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24902-127">CommonParameters</span></span>
<span data-ttu-id="24902-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24902-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24902-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24902-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24902-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="24902-130">INPUTS</span></span>

### <span data-ttu-id="24902-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="24902-131">None</span></span>

## <span data-ttu-id="24902-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="24902-132">OUTPUTS</span></span>

### <span data-ttu-id="24902-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="24902-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="24902-134">Notas</span><span class="sxs-lookup"><span data-stu-id="24902-134">NOTES</span></span>

## <span data-ttu-id="24902-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24902-135">RELATED LINKS</span></span>
