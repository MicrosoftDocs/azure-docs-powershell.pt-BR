---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 6561037b9174fd732d616f425324c164529e6367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887363"
---
# <span data-ttu-id="57c26-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="57c26-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="57c26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57c26-102">SYNOPSIS</span></span>
<span data-ttu-id="57c26-103">Obtém uma conexão cruzada do Azure ExpressRoute do Azure.</span><span class="sxs-lookup"><span data-stu-id="57c26-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="57c26-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57c26-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57c26-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57c26-105">DESCRIPTION</span></span>
<span data-ttu-id="57c26-106">O cmdlet **Get-AzExpressRouteCrossConnection** é usado para recuperar um objeto de conexão cruzada ExpressRoute da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="57c26-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="57c26-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="57c26-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="57c26-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57c26-108">EXAMPLES</span></span>

### <span data-ttu-id="57c26-109">Exemplo 1: Obter a conexão cruzada ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="57c26-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="57c26-110">Exemplo 2: Listar as conexões entre ExpressRoute usando um filtro</span><span class="sxs-lookup"><span data-stu-id="57c26-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="57c26-111">Este cmdlet listará todas as conexões entre ExpressRoute que começam com "test"</span><span class="sxs-lookup"><span data-stu-id="57c26-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="57c26-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57c26-112">PARAMETERS</span></span>

### <span data-ttu-id="57c26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c26-113">-DefaultProfile</span></span>
<span data-ttu-id="57c26-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="57c26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57c26-115">-Name</span><span class="sxs-lookup"><span data-stu-id="57c26-115">-Name</span></span>
<span data-ttu-id="57c26-116">O nome da conexão cruzada ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="57c26-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="57c26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c26-117">-ResourceGroupName</span></span>
<span data-ttu-id="57c26-118">O nome do grupo de recursos que contém a conexão cruzada ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="57c26-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="57c26-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c26-119">CommonParameters</span></span>
<span data-ttu-id="57c26-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c26-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c26-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57c26-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c26-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57c26-122">INPUTS</span></span>

### <span data-ttu-id="57c26-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="57c26-123">None</span></span>
<span data-ttu-id="57c26-124">Este cmdlet não aceita qualquer entrada.</span><span class="sxs-lookup"><span data-stu-id="57c26-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57c26-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57c26-125">OUTPUTS</span></span>

### <span data-ttu-id="57c26-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="57c26-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="57c26-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="57c26-127">NOTES</span></span>

## <span data-ttu-id="57c26-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57c26-128">RELATED LINKS</span></span>

[<span data-ttu-id="57c26-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="57c26-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)