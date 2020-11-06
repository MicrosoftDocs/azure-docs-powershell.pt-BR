---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: 2217a6940e5f740c2499e95ff05f67c7144cbc3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602299"
---
# <span data-ttu-id="c1088-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="c1088-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="c1088-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1088-102">SYNOPSIS</span></span>
<span data-ttu-id="c1088-103">Obtém os espaços de trabalho em uma coleção do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="c1088-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1088-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1088-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1088-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1088-105">DESCRIPTION</span></span>
<span data-ttu-id="c1088-106">O cmdlet **Get-AzureRmPowerBIWorkspace** Obtém os espaços de trabalho em uma coleção do espaço de trabalho do Power bi.</span><span class="sxs-lookup"><span data-stu-id="c1088-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c1088-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1088-107">EXAMPLES</span></span>

### <span data-ttu-id="c1088-108">Exemplo 1: obter espaços de trabalho de uma coleção de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c1088-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c1088-109">Esse comando obtém os espaços de trabalho que pertencem ao conjunto de espaço de trabalho chamado WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c1088-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c1088-110">OS</span><span class="sxs-lookup"><span data-stu-id="c1088-110">PARAMETERS</span></span>

### <span data-ttu-id="c1088-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1088-111">-DefaultProfile</span></span>
<span data-ttu-id="c1088-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c1088-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1088-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1088-113">-ResourceGroupName</span></span>
<span data-ttu-id="c1088-114">Especifica o nome do grupo de recursos ao qual a coleção de espaço de trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="c1088-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="c1088-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c1088-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c1088-116">Especifica o nome da coleção de espaço de trabalho para a qual esse cmdlet obtém espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1088-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="c1088-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1088-117">CommonParameters</span></span>
<span data-ttu-id="c1088-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1088-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1088-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1088-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1088-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1088-120">INPUTS</span></span>

### <span data-ttu-id="c1088-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c1088-121">System.String</span></span>

## <span data-ttu-id="c1088-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1088-122">OUTPUTS</span></span>

### <span data-ttu-id="c1088-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c1088-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="c1088-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1088-124">NOTES</span></span>

## <span data-ttu-id="c1088-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1088-125">RELATED LINKS</span></span>

[<span data-ttu-id="c1088-126">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c1088-126">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


