---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118530"
---
# <span data-ttu-id="1562c-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1562c-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="1562c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1562c-102">SYNOPSIS</span></span>
<span data-ttu-id="1562c-103">Verifica a existência de um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1562c-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="1562c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1562c-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1562c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1562c-105">DESCRIPTION</span></span>
<span data-ttu-id="1562c-106">O cmdlet **Test-AzSynapseWorkspace** verifica a existência de um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1562c-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="1562c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1562c-107">EXAMPLES</span></span>

### <span data-ttu-id="1562c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1562c-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="1562c-109">Esse comando verifica a existência de um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1562c-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="1562c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1562c-110">PARAMETERS</span></span>

### <span data-ttu-id="1562c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1562c-111">-DefaultProfile</span></span>
<span data-ttu-id="1562c-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1562c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1562c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1562c-113">-Name</span></span>
<span data-ttu-id="1562c-114">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="1562c-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1562c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1562c-115">-ResourceGroupName</span></span>
<span data-ttu-id="1562c-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1562c-116">Resource group name.</span></span>

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

### <span data-ttu-id="1562c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1562c-117">CommonParameters</span></span>
<span data-ttu-id="1562c-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1562c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1562c-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1562c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1562c-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="1562c-120">INPUTS</span></span>

### <span data-ttu-id="1562c-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1562c-121">None</span></span>

## <span data-ttu-id="1562c-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="1562c-122">OUTPUTS</span></span>

### <span data-ttu-id="1562c-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="1562c-123">System.Object</span></span>
## <span data-ttu-id="1562c-124">Notas</span><span class="sxs-lookup"><span data-stu-id="1562c-124">NOTES</span></span>

## <span data-ttu-id="1562c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1562c-125">RELATED LINKS</span></span>
