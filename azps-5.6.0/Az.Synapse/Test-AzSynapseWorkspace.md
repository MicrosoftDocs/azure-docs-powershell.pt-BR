---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: e92b4d20e89df451c483bc0b4bdccb83fdc8a140
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893052"
---
# <span data-ttu-id="986a1-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="986a1-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="986a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986a1-102">SYNOPSIS</span></span>
<span data-ttu-id="986a1-103">Verifica a existência de um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="986a1-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="986a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="986a1-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="986a1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="986a1-105">DESCRIPTION</span></span>
<span data-ttu-id="986a1-106">O cmdlet **Test-AzSynapseWorkspace** verifica a existência de um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="986a1-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="986a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="986a1-107">EXAMPLES</span></span>

### <span data-ttu-id="986a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="986a1-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="986a1-109">Este comando verifica a existência de um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="986a1-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="986a1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="986a1-110">PARAMETERS</span></span>

### <span data-ttu-id="986a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986a1-111">-DefaultProfile</span></span>
<span data-ttu-id="986a1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="986a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="986a1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="986a1-113">-Name</span></span>
<span data-ttu-id="986a1-114">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="986a1-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="986a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="986a1-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="986a1-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986a1-117">CommonParameters</span></span>
<span data-ttu-id="986a1-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="986a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986a1-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="986a1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986a1-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="986a1-120">INPUTS</span></span>

### <span data-ttu-id="986a1-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="986a1-121">None</span></span>

## <span data-ttu-id="986a1-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="986a1-122">OUTPUTS</span></span>

### <span data-ttu-id="986a1-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="986a1-123">System.Object</span></span>
## <span data-ttu-id="986a1-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="986a1-124">NOTES</span></span>

## <span data-ttu-id="986a1-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="986a1-125">RELATED LINKS</span></span>
