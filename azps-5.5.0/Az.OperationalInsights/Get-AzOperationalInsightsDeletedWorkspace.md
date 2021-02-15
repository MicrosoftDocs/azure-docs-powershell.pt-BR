---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115019"
---
# <span data-ttu-id="2162b-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="2162b-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="2162b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2162b-102">SYNOPSIS</span></span>
<span data-ttu-id="2162b-103">Listar espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="2162b-103">List deleted workspaces.</span></span>

## <span data-ttu-id="2162b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2162b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2162b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2162b-105">DESCRIPTION</span></span>
<span data-ttu-id="2162b-106">Listar espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="2162b-106">List deleted workspaces.</span></span>

## <span data-ttu-id="2162b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2162b-107">EXAMPLES</span></span>

### <span data-ttu-id="2162b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2162b-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="2162b-109">Listar espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="2162b-109">List deleted workspaces.</span></span>

## <span data-ttu-id="2162b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2162b-110">PARAMETERS</span></span>

### <span data-ttu-id="2162b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2162b-111">-DefaultProfile</span></span>
<span data-ttu-id="2162b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2162b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2162b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2162b-113">-ResourceGroupName</span></span>
<span data-ttu-id="2162b-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2162b-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2162b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2162b-115">CommonParameters</span></span>
<span data-ttu-id="2162b-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2162b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2162b-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2162b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2162b-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="2162b-118">INPUTS</span></span>

### <span data-ttu-id="2162b-119">System.String</span><span class="sxs-lookup"><span data-stu-id="2162b-119">System.String</span></span>

## <span data-ttu-id="2162b-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="2162b-120">OUTPUTS</span></span>

### <span data-ttu-id="2162b-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2162b-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="2162b-122">Notas</span><span class="sxs-lookup"><span data-stu-id="2162b-122">NOTES</span></span>

## <span data-ttu-id="2162b-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2162b-123">RELATED LINKS</span></span>
