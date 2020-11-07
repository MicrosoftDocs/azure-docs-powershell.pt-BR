---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943461"
---
# <span data-ttu-id="04396-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="04396-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="04396-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04396-102">SYNOPSIS</span></span>
<span data-ttu-id="04396-103">Obtém uma conexão cruzada do Azure ExpressRoute do Azure.</span><span class="sxs-lookup"><span data-stu-id="04396-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="04396-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04396-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04396-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04396-105">DESCRIPTION</span></span>
<span data-ttu-id="04396-106">O cmdlet **Get-AzExpressRouteCrossConnection** é usado para recuperar um objeto de conexão cruzada do ExpressRoute da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="04396-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="04396-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="04396-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="04396-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04396-108">EXAMPLES</span></span>

### <span data-ttu-id="04396-109">Exemplo 1: obter a conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="04396-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="04396-110">Exemplo 2: listar as conexões cruzadas do ExpressRoute usando um filtro</span><span class="sxs-lookup"><span data-stu-id="04396-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="04396-111">Este cmdlet listará todas as conexões cruzadas do ExpressRoute que começam com "Test"</span><span class="sxs-lookup"><span data-stu-id="04396-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="04396-112">OS</span><span class="sxs-lookup"><span data-stu-id="04396-112">PARAMETERS</span></span>

### <span data-ttu-id="04396-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04396-113">-DefaultProfile</span></span>
<span data-ttu-id="04396-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04396-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04396-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="04396-115">-Name</span></span>
<span data-ttu-id="04396-116">O nome da conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="04396-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="04396-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04396-117">-ResourceGroupName</span></span>
<span data-ttu-id="04396-118">O nome do grupo de recursos que contém a conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="04396-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="04396-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04396-119">CommonParameters</span></span>
<span data-ttu-id="04396-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04396-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04396-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04396-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04396-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04396-122">INPUTS</span></span>

### <span data-ttu-id="04396-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="04396-123">None</span></span>
<span data-ttu-id="04396-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="04396-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04396-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04396-125">OUTPUTS</span></span>

### <span data-ttu-id="04396-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="04396-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="04396-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04396-127">NOTES</span></span>

## <span data-ttu-id="04396-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04396-128">RELATED LINKS</span></span>

[<span data-ttu-id="04396-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="04396-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)