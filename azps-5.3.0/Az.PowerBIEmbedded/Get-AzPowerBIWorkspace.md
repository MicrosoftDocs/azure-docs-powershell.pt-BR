---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429501"
---
# <span data-ttu-id="9ab87-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ab87-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="9ab87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ab87-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab87-103">Obtém os espaços de trabalho em uma coleção do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="9ab87-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="9ab87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ab87-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ab87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ab87-105">DESCRIPTION</span></span>
<span data-ttu-id="9ab87-106">O cmdlet **Get-AzPowerBIWorkspace** Obtém os espaços de trabalho em uma coleção do espaço de trabalho do Power bi.</span><span class="sxs-lookup"><span data-stu-id="9ab87-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="9ab87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ab87-107">EXAMPLES</span></span>

### <span data-ttu-id="9ab87-108">Exemplo 1: obter espaços de trabalho de uma coleção de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="9ab87-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="9ab87-109">Esse comando obtém os espaços de trabalho que pertencem ao conjunto de espaço de trabalho chamado WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="9ab87-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="9ab87-110">OS</span><span class="sxs-lookup"><span data-stu-id="9ab87-110">PARAMETERS</span></span>

### <span data-ttu-id="9ab87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab87-111">-DefaultProfile</span></span>
<span data-ttu-id="9ab87-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9ab87-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ab87-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab87-113">-ResourceGroupName</span></span>
<span data-ttu-id="9ab87-114">Especifica o nome do grupo de recursos ao qual a coleção de espaço de trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="9ab87-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="9ab87-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="9ab87-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="9ab87-116">Especifica o nome da coleção de espaço de trabalho para a qual esse cmdlet obtém espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9ab87-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="9ab87-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab87-117">CommonParameters</span></span>
<span data-ttu-id="9ab87-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab87-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab87-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab87-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab87-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ab87-120">INPUTS</span></span>

### <span data-ttu-id="9ab87-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9ab87-121">System.String</span></span>

## <span data-ttu-id="9ab87-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ab87-122">OUTPUTS</span></span>

### <span data-ttu-id="9ab87-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ab87-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="9ab87-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ab87-124">NOTES</span></span>

## <span data-ttu-id="9ab87-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ab87-125">RELATED LINKS</span></span>

[<span data-ttu-id="9ab87-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9ab87-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


