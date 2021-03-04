---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 06e17c012f52883d5e160698bb6f858f4644af6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888212"
---
# <span data-ttu-id="b9451-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b9451-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b9451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9451-102">SYNOPSIS</span></span>
<span data-ttu-id="b9451-103">Obtém as chaves de acesso atuais associadas a uma coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="b9451-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="b9451-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b9451-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9451-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b9451-105">DESCRIPTION</span></span>
<span data-ttu-id="b9451-106">O cmdlet **Get-AzPowerBIWorkspaceCollectionAccessKey** obtém as chaves de acesso atuais associadas a uma coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="b9451-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="b9451-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9451-107">EXAMPLES</span></span>

### <span data-ttu-id="b9451-108">Exemplo 1: Obter chaves de acesso</span><span class="sxs-lookup"><span data-stu-id="b9451-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="b9451-109">Este comando obtém chaves de acesso para a coleção de espaços de trabalho chamada WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b9451-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b9451-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b9451-110">PARAMETERS</span></span>

### <span data-ttu-id="b9451-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9451-111">-DefaultProfile</span></span>
<span data-ttu-id="b9451-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b9451-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9451-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9451-113">-ResourceGroupName</span></span>
<span data-ttu-id="b9451-114">Especifica o nome do grupo de recursos da coleção.</span><span class="sxs-lookup"><span data-stu-id="b9451-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="b9451-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b9451-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b9451-116">Especifica o nome da coleção de espaços de trabalho do Power BI no qual esse cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="b9451-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b9451-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9451-117">CommonParameters</span></span>
<span data-ttu-id="b9451-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9451-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9451-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9451-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9451-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9451-120">INPUTS</span></span>

### <span data-ttu-id="b9451-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b9451-121">System.String</span></span>

## <span data-ttu-id="b9451-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b9451-122">OUTPUTS</span></span>

### <span data-ttu-id="b9451-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b9451-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b9451-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="b9451-124">NOTES</span></span>

## <span data-ttu-id="b9451-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9451-125">RELATED LINKS</span></span>

[<span data-ttu-id="b9451-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b9451-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


