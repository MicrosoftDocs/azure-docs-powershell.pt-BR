---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3be81626dc48f66fd7aac71c23c2cd9168dab336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892435"
---
# <span data-ttu-id="6373e-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6373e-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="6373e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6373e-102">SYNOPSIS</span></span>
<span data-ttu-id="6373e-103">Obtém os parâmetros ipsec vpn definidos no Virtual Network Gateway for Point to site connections.</span><span class="sxs-lookup"><span data-stu-id="6373e-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="6373e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6373e-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6373e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6373e-105">DESCRIPTION</span></span>
<span data-ttu-id="6373e-106">O Gateway de Rede Virtual é o objeto que representa seu gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="6373e-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="6373e-107">O cmdlet **Get-AzVpnClientIpsecParameter** retorna o objeto de seus parâmetros ipsec vpn definidos no gateway no Azure com base no Nome do Gateway e no Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="6373e-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="6373e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6373e-108">EXAMPLES</span></span>

### <span data-ttu-id="6373e-109">Exemplo 1: obtém os parâmetros ipsec vpn definidos no Virtual Network Gateway for Point to site connections.</span><span class="sxs-lookup"><span data-stu-id="6373e-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6373e-110">Retorna o objeto dos parâmetros ipsec vpn definidos no Gateway de Rede Virtual com o nome "myGateway" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="6373e-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="6373e-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6373e-111">PARAMETERS</span></span>

### <span data-ttu-id="6373e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6373e-112">-DefaultProfile</span></span>
<span data-ttu-id="6373e-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6373e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6373e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6373e-114">-Name</span></span>
<span data-ttu-id="6373e-115">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6373e-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6373e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6373e-116">-ResourceGroupName</span></span>
<span data-ttu-id="6373e-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6373e-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6373e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6373e-118">CommonParameters</span></span>
<span data-ttu-id="6373e-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6373e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6373e-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6373e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6373e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6373e-121">INPUTS</span></span>

### <span data-ttu-id="6373e-122">System.String</span><span class="sxs-lookup"><span data-stu-id="6373e-122">System.String</span></span>

## <span data-ttu-id="6373e-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6373e-123">OUTPUTS</span></span>

### <span data-ttu-id="6373e-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="6373e-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="6373e-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="6373e-125">NOTES</span></span>

## <span data-ttu-id="6373e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6373e-126">RELATED LINKS</span></span>

[<span data-ttu-id="6373e-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6373e-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="6373e-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6373e-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="6373e-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6373e-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
