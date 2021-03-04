---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: a4ac55c3c00ba35fa53f6e9a338712d02e507ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888450"
---
# <span data-ttu-id="38ff8-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="38ff8-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="38ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="38ff8-103">Listar espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="38ff8-103">List deleted workspaces.</span></span>

## <span data-ttu-id="38ff8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38ff8-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38ff8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="38ff8-106">Listar espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="38ff8-106">List deleted workspaces.</span></span>

## <span data-ttu-id="38ff8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="38ff8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38ff8-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="38ff8-109">Listar espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="38ff8-109">List deleted workspaces.</span></span>

## <span data-ttu-id="38ff8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38ff8-110">PARAMETERS</span></span>

### <span data-ttu-id="38ff8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ff8-111">-DefaultProfile</span></span>
<span data-ttu-id="38ff8-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38ff8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ff8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ff8-113">-ResourceGroupName</span></span>
<span data-ttu-id="38ff8-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38ff8-114">The resource group name.</span></span>

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

### <span data-ttu-id="38ff8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ff8-115">CommonParameters</span></span>
<span data-ttu-id="38ff8-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ff8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ff8-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38ff8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ff8-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38ff8-118">INPUTS</span></span>

### <span data-ttu-id="38ff8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="38ff8-119">System.String</span></span>

## <span data-ttu-id="38ff8-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38ff8-120">OUTPUTS</span></span>

### <span data-ttu-id="38ff8-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="38ff8-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="38ff8-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="38ff8-122">NOTES</span></span>

## <span data-ttu-id="38ff8-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38ff8-123">RELATED LINKS</span></span>
