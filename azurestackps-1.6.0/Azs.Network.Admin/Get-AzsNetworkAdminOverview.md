---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601776"
---
# <span data-ttu-id="68d6b-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="68d6b-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="68d6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="68d6b-103">Obtenha uma visão geral do estado do provedor de recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="68d6b-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="68d6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68d6b-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="68d6b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="68d6b-106">Obtenha uma visão geral do estado do provedor de recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="68d6b-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="68d6b-107">As propriedades individuais fornecem contas detalhadas de uso de recursos e integridade por componente.</span><span class="sxs-lookup"><span data-stu-id="68d6b-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="68d6b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68d6b-108">EXAMPLES</span></span>

### <span data-ttu-id="68d6b-109">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="68d6b-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="68d6b-110">Obter visão geral do administrador de rede.</span><span class="sxs-lookup"><span data-stu-id="68d6b-110">Get network admin overview.</span></span>

### <span data-ttu-id="68d6b-111">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="68d6b-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="68d6b-112">Obter o uso do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="68d6b-112">Get public ip address usage.</span></span>

## <span data-ttu-id="68d6b-113">OS</span><span class="sxs-lookup"><span data-stu-id="68d6b-113">PARAMETERS</span></span>

### <span data-ttu-id="68d6b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d6b-114">CommonParameters</span></span>
<span data-ttu-id="68d6b-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68d6b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d6b-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68d6b-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d6b-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68d6b-117">INPUTS</span></span>

## <span data-ttu-id="68d6b-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68d6b-118">OUTPUTS</span></span>

### <span data-ttu-id="68d6b-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="68d6b-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="68d6b-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68d6b-120">NOTES</span></span>

## <span data-ttu-id="68d6b-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68d6b-121">RELATED LINKS</span></span>

