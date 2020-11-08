---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114040"
---
# <span data-ttu-id="a5e35-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5e35-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="a5e35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5e35-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e35-103">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="a5e35-103">List deleted workspaces.</span></span>

## <span data-ttu-id="a5e35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5e35-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5e35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5e35-105">DESCRIPTION</span></span>
<span data-ttu-id="a5e35-106">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="a5e35-106">List deleted workspaces.</span></span>

## <span data-ttu-id="a5e35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5e35-107">EXAMPLES</span></span>

### <span data-ttu-id="a5e35-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5e35-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="a5e35-109">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="a5e35-109">List deleted workspaces.</span></span>

## <span data-ttu-id="a5e35-110">OS</span><span class="sxs-lookup"><span data-stu-id="a5e35-110">PARAMETERS</span></span>

### <span data-ttu-id="a5e35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e35-111">-DefaultProfile</span></span>
<span data-ttu-id="a5e35-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e35-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e35-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e35-113">-ResourceGroupName</span></span>
<span data-ttu-id="a5e35-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5e35-114">The resource group name.</span></span>

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

### <span data-ttu-id="a5e35-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e35-115">CommonParameters</span></span>
<span data-ttu-id="a5e35-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e35-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e35-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e35-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e35-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5e35-118">INPUTS</span></span>

### <span data-ttu-id="a5e35-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e35-119">System.String</span></span>

## <span data-ttu-id="a5e35-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5e35-120">OUTPUTS</span></span>

### <span data-ttu-id="a5e35-121">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5e35-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a5e35-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5e35-122">NOTES</span></span>

## <span data-ttu-id="a5e35-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5e35-123">RELATED LINKS</span></span>
