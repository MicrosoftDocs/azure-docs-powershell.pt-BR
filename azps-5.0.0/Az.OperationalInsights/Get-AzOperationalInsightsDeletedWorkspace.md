---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124442"
---
# <span data-ttu-id="a2c8f-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2c8f-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="a2c8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c8f-103">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="a2c8f-103">List deleted workspaces.</span></span>

## <span data-ttu-id="a2c8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2c8f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c8f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c8f-106">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="a2c8f-106">List deleted workspaces.</span></span>

## <span data-ttu-id="a2c8f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2c8f-107">EXAMPLES</span></span>

### <span data-ttu-id="a2c8f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2c8f-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="a2c8f-109">Liste os espaços de trabalho excluídos.</span><span class="sxs-lookup"><span data-stu-id="a2c8f-109">List deleted workspaces.</span></span>

## <span data-ttu-id="a2c8f-110">OS</span><span class="sxs-lookup"><span data-stu-id="a2c8f-110">PARAMETERS</span></span>

### <span data-ttu-id="a2c8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c8f-111">-DefaultProfile</span></span>
<span data-ttu-id="a2c8f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c8f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c8f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c8f-113">-ResourceGroupName</span></span>
<span data-ttu-id="a2c8f-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a2c8f-114">The resource group name.</span></span>

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

### <span data-ttu-id="a2c8f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c8f-115">CommonParameters</span></span>
<span data-ttu-id="a2c8f-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c8f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c8f-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2c8f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c8f-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2c8f-118">INPUTS</span></span>

### <span data-ttu-id="a2c8f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a2c8f-119">System.String</span></span>

## <span data-ttu-id="a2c8f-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2c8f-120">OUTPUTS</span></span>

### <span data-ttu-id="a2c8f-121">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2c8f-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a2c8f-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2c8f-122">NOTES</span></span>

## <span data-ttu-id="a2c8f-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2c8f-123">RELATED LINKS</span></span>
