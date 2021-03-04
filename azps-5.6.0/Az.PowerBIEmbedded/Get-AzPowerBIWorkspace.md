---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: d9c93bc487817d99b217519453dea10543852a1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888213"
---
# <span data-ttu-id="066d5-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="066d5-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="066d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="066d5-102">SYNOPSIS</span></span>
<span data-ttu-id="066d5-103">Obtém os espaços de trabalho em uma coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="066d5-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="066d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="066d5-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="066d5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="066d5-105">DESCRIPTION</span></span>
<span data-ttu-id="066d5-106">O cmdlet **Get-AzPowerBIWorkspace** obtém os espaços de trabalho em uma coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="066d5-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="066d5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="066d5-107">EXAMPLES</span></span>

### <span data-ttu-id="066d5-108">Exemplo 1: Obter espaços de trabalho de uma coleção de espaços de trabalho</span><span class="sxs-lookup"><span data-stu-id="066d5-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="066d5-109">Este comando obtém os espaços de trabalho que pertencem à coleção de espaços de trabalho chamada WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="066d5-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="066d5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="066d5-110">PARAMETERS</span></span>

### <span data-ttu-id="066d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066d5-111">-DefaultProfile</span></span>
<span data-ttu-id="066d5-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="066d5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="066d5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="066d5-113">-ResourceGroupName</span></span>
<span data-ttu-id="066d5-114">Especifica o nome do grupo de recursos ao qual a coleção de espaços de trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="066d5-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="066d5-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="066d5-116">Especifica o nome da coleção de espaços de trabalho para a qual este cmdlet obtém espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="066d5-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066d5-117">CommonParameters</span></span>
<span data-ttu-id="066d5-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066d5-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="066d5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066d5-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="066d5-120">INPUTS</span></span>

### <span data-ttu-id="066d5-121">System.String</span><span class="sxs-lookup"><span data-stu-id="066d5-121">System.String</span></span>

## <span data-ttu-id="066d5-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="066d5-122">OUTPUTS</span></span>

### <span data-ttu-id="066d5-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="066d5-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="066d5-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="066d5-124">NOTES</span></span>

## <span data-ttu-id="066d5-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="066d5-125">RELATED LINKS</span></span>

[<span data-ttu-id="066d5-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="066d5-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


