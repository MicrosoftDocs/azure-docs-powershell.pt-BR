---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772026"
---
# <span data-ttu-id="862da-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="862da-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="862da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="862da-102">SYNOPSIS</span></span>
<span data-ttu-id="862da-103">Obtém uma conexão cruzada do Azure ExpressRoute do Azure.</span><span class="sxs-lookup"><span data-stu-id="862da-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="862da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="862da-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="862da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="862da-105">DESCRIPTION</span></span>
<span data-ttu-id="862da-106">O cmdlet **Get-AzExpressRouteCrossConnection** é usado para recuperar um objeto de conexão cruzada do ExpressRoute da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="862da-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="862da-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="862da-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="862da-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="862da-108">EXAMPLES</span></span>

### <span data-ttu-id="862da-109">Exemplo 1: obter a conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="862da-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="862da-110">Exemplo 2: listar as conexões cruzadas do ExpressRoute usando um filtro</span><span class="sxs-lookup"><span data-stu-id="862da-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="862da-111">Este cmdlet listará todas as conexões cruzadas do ExpressRoute que começam com "Test"</span><span class="sxs-lookup"><span data-stu-id="862da-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="862da-112">OS</span><span class="sxs-lookup"><span data-stu-id="862da-112">PARAMETERS</span></span>

### <span data-ttu-id="862da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862da-113">-DefaultProfile</span></span>
<span data-ttu-id="862da-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="862da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="862da-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="862da-115">-Name</span></span>
<span data-ttu-id="862da-116">O nome da conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="862da-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="862da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="862da-117">-ResourceGroupName</span></span>
<span data-ttu-id="862da-118">O nome do grupo de recursos que contém a conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="862da-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="862da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862da-119">CommonParameters</span></span>
<span data-ttu-id="862da-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="862da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862da-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="862da-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862da-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="862da-122">INPUTS</span></span>

### <span data-ttu-id="862da-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="862da-123">None</span></span>
<span data-ttu-id="862da-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="862da-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="862da-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="862da-125">OUTPUTS</span></span>

### <span data-ttu-id="862da-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="862da-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="862da-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="862da-127">NOTES</span></span>

## <span data-ttu-id="862da-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="862da-128">RELATED LINKS</span></span>

[<span data-ttu-id="862da-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="862da-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)