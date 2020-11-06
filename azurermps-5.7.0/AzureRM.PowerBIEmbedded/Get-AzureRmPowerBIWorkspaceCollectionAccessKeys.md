---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 11c1e3c19a6f5767fcfe1120cfa3561a73885f5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428123"
---
# <span data-ttu-id="1c9a7-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1c9a7-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="1c9a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9a7-103">Obtém as teclas de acesso atuais associadas a uma coleção do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c9a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c9a7-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c9a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c9a7-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9a7-106">O cmdlet **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** Obtém as teclas de acesso atuais associadas a uma coleção do espaço de trabalho do Power bi.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="1c9a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c9a7-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9a7-108">Exemplo 1: obter as teclas de acesso</span><span class="sxs-lookup"><span data-stu-id="1c9a7-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="1c9a7-109">Esse comando obtém teclas de acesso para a coleção de espaço de trabalho chamada WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="1c9a7-110">OS</span><span class="sxs-lookup"><span data-stu-id="1c9a7-110">PARAMETERS</span></span>

### <span data-ttu-id="1c9a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9a7-111">-DefaultProfile</span></span>
<span data-ttu-id="1c9a7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1c9a7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9a7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c9a7-113">-ResourceGroupName</span></span>
<span data-ttu-id="1c9a7-114">Especifica o nome do grupo de recursos da coleção.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-114">Specifies the name of the resource group of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9a7-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1c9a7-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="1c9a7-116">Especifica o nome da coleção do espaço de trabalho do Power BI na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9a7-117">CommonParameters</span></span>
<span data-ttu-id="1c9a7-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9a7-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9a7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9a7-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c9a7-120">INPUTS</span></span>

### <span data-ttu-id="1c9a7-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1c9a7-121">None</span></span>
<span data-ttu-id="1c9a7-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c9a7-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c9a7-123">OUTPUTS</span></span>

### <span data-ttu-id="1c9a7-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="1c9a7-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="1c9a7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c9a7-125">NOTES</span></span>

## <span data-ttu-id="1c9a7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c9a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="1c9a7-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1c9a7-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


