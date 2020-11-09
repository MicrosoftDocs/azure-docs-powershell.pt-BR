---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284097"
---
# <span data-ttu-id="ead21-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="ead21-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="ead21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ead21-102">SYNOPSIS</span></span>
<span data-ttu-id="ead21-103">Obtém uma configuração de link ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ead21-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="ead21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ead21-104">SYNTAX</span></span>

### <span data-ttu-id="ead21-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ead21-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ead21-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead21-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ead21-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ead21-107">DESCRIPTION</span></span>
<span data-ttu-id="ead21-108">O cmdlet **Get-AzExpressRoutePortLinkConfig** recupera a configuração de um link de um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ead21-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="ead21-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ead21-109">EXAMPLES</span></span>

### <span data-ttu-id="ead21-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ead21-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="ead21-111">Obtém a configuração LINK1 do ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="ead21-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="ead21-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ead21-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="ead21-113">Obtém a configuração do link com o ResourceId $id em ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="ead21-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="ead21-114">OS</span><span class="sxs-lookup"><span data-stu-id="ead21-114">PARAMETERS</span></span>

### <span data-ttu-id="ead21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead21-115">-DefaultProfile</span></span>
<span data-ttu-id="ead21-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ead21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead21-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ead21-117">-ExpressRoutePort</span></span>
<span data-ttu-id="ead21-118">A referência do recurso ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ead21-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead21-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ead21-119">-Name</span></span>
<span data-ttu-id="ead21-120">Nome do link.</span><span class="sxs-lookup"><span data-stu-id="ead21-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead21-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ead21-121">-ResourceId</span></span>
<span data-ttu-id="ead21-122">ResourceId do link.</span><span class="sxs-lookup"><span data-stu-id="ead21-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead21-123">CommonParameters</span></span>
<span data-ttu-id="ead21-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead21-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ead21-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead21-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ead21-126">INPUTS</span></span>

### <span data-ttu-id="ead21-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ead21-127">System.String</span></span>

### <span data-ttu-id="ead21-128">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ead21-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ead21-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ead21-129">OUTPUTS</span></span>

### <span data-ttu-id="ead21-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="ead21-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="ead21-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ead21-131">NOTES</span></span>

## <span data-ttu-id="ead21-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ead21-132">RELATED LINKS</span></span>
