---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434567"
---
# <span data-ttu-id="2648d-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="2648d-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="2648d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2648d-102">SYNOPSIS</span></span>
<span data-ttu-id="2648d-103">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="2648d-103">List deleted workspaces.</span></span>

## <span data-ttu-id="2648d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2648d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2648d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2648d-105">DESCRIPTION</span></span>
<span data-ttu-id="2648d-106">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="2648d-106">List deleted workspaces.</span></span>

## <span data-ttu-id="2648d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2648d-107">EXAMPLES</span></span>

### <span data-ttu-id="2648d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2648d-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="2648d-109">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="2648d-109">List deleted workspaces.</span></span>

## <span data-ttu-id="2648d-110">OS</span><span class="sxs-lookup"><span data-stu-id="2648d-110">PARAMETERS</span></span>

### <span data-ttu-id="2648d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2648d-111">-DefaultProfile</span></span>
<span data-ttu-id="2648d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2648d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2648d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2648d-113">-ResourceGroupName</span></span>
<span data-ttu-id="2648d-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2648d-114">The resource group name.</span></span>

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

### <span data-ttu-id="2648d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2648d-115">CommonParameters</span></span>
<span data-ttu-id="2648d-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2648d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2648d-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2648d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2648d-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2648d-118">INPUTS</span></span>

### <span data-ttu-id="2648d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="2648d-119">System.String</span></span>

## <span data-ttu-id="2648d-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2648d-120">OUTPUTS</span></span>

### <span data-ttu-id="2648d-121">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2648d-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="2648d-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2648d-122">NOTES</span></span>

## <span data-ttu-id="2648d-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2648d-123">RELATED LINKS</span></span>
