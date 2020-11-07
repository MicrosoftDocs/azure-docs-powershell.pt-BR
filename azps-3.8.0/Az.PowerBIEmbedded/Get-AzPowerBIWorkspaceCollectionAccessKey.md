---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940627"
---
# <span data-ttu-id="95847-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="95847-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="95847-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95847-102">SYNOPSIS</span></span>
<span data-ttu-id="95847-103">Obtém as teclas de acesso atuais associadas a uma coleção do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="95847-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="95847-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95847-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95847-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95847-105">DESCRIPTION</span></span>
<span data-ttu-id="95847-106">O cmdlet **Get-AzPowerBIWorkspaceCollectionAccessKey** Obtém as teclas de acesso atuais associadas a uma coleção do espaço de trabalho do Power bi.</span><span class="sxs-lookup"><span data-stu-id="95847-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="95847-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95847-107">EXAMPLES</span></span>

### <span data-ttu-id="95847-108">Exemplo 1: obter as teclas de acesso</span><span class="sxs-lookup"><span data-stu-id="95847-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="95847-109">Esse comando obtém teclas de acesso para a coleção de espaço de trabalho chamada WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="95847-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="95847-110">OS</span><span class="sxs-lookup"><span data-stu-id="95847-110">PARAMETERS</span></span>

### <span data-ttu-id="95847-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95847-111">-DefaultProfile</span></span>
<span data-ttu-id="95847-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="95847-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95847-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95847-113">-ResourceGroupName</span></span>
<span data-ttu-id="95847-114">Especifica o nome do grupo de recursos da coleção.</span><span class="sxs-lookup"><span data-stu-id="95847-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="95847-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="95847-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="95847-116">Especifica o nome da coleção do espaço de trabalho do Power BI na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="95847-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="95847-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95847-117">CommonParameters</span></span>
<span data-ttu-id="95847-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95847-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95847-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95847-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95847-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95847-120">INPUTS</span></span>

### <span data-ttu-id="95847-121">System. String</span><span class="sxs-lookup"><span data-stu-id="95847-121">System.String</span></span>

## <span data-ttu-id="95847-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95847-122">OUTPUTS</span></span>

### <span data-ttu-id="95847-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="95847-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="95847-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95847-124">NOTES</span></span>

## <span data-ttu-id="95847-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95847-125">RELATED LINKS</span></span>

[<span data-ttu-id="95847-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="95847-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


