---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260486"
---
# <span data-ttu-id="a1dd0-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="a1dd0-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="a1dd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="a1dd0-103">Obtém uma configuração de link ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a1dd0-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="a1dd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1dd0-104">SYNTAX</span></span>

### <span data-ttu-id="a1dd0-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1dd0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1dd0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1dd0-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1dd0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1dd0-107">DESCRIPTION</span></span>
<span data-ttu-id="a1dd0-108">O cmdlet **Get-AzExpressRoutePortLinkConfig** recupera a configuração de um link de um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a1dd0-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="a1dd0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1dd0-109">EXAMPLES</span></span>

### <span data-ttu-id="a1dd0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1dd0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="a1dd0-111">Obtém a configuração LINK1 do ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="a1dd0-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="a1dd0-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a1dd0-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="a1dd0-113">Obtém a configuração do link com o ResourceId $id em ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="a1dd0-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="a1dd0-114">OS</span><span class="sxs-lookup"><span data-stu-id="a1dd0-114">PARAMETERS</span></span>

### <span data-ttu-id="a1dd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1dd0-115">-DefaultProfile</span></span>
<span data-ttu-id="a1dd0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dd0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1dd0-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a1dd0-117">-ExpressRoutePort</span></span>
<span data-ttu-id="a1dd0-118">A referência do recurso ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a1dd0-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="a1dd0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1dd0-119">-Name</span></span>
<span data-ttu-id="a1dd0-120">Nome do link.</span><span class="sxs-lookup"><span data-stu-id="a1dd0-120">Name of the link.</span></span>

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

### <span data-ttu-id="a1dd0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1dd0-121">-ResourceId</span></span>
<span data-ttu-id="a1dd0-122">ResourceId do link.</span><span class="sxs-lookup"><span data-stu-id="a1dd0-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="a1dd0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1dd0-123">CommonParameters</span></span>
<span data-ttu-id="a1dd0-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1dd0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1dd0-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1dd0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1dd0-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1dd0-126">INPUTS</span></span>

### <span data-ttu-id="a1dd0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a1dd0-127">System.String</span></span>

### <span data-ttu-id="a1dd0-128">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a1dd0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a1dd0-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1dd0-129">OUTPUTS</span></span>

### <span data-ttu-id="a1dd0-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="a1dd0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="a1dd0-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1dd0-131">NOTES</span></span>

## <span data-ttu-id="a1dd0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1dd0-132">RELATED LINKS</span></span>
