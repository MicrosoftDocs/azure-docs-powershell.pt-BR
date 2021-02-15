---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114696"
---
# <span data-ttu-id="e9d4d-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e9d4d-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="e9d4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d4d-103">Obtém os parâmetros Ipsec vpn definidos no Gateway de Rede Virtual para conexões ponto a site.</span><span class="sxs-lookup"><span data-stu-id="e9d4d-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="e9d4d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9d4d-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9d4d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9d4d-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d4d-106">O Gateway de Rede Virtual é o objeto que representa seu gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d4d-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="e9d4d-107">O cmdlet **Get-AzVpnClientIpsecParameter** retorna o objeto dos parâmetros ipsec de vpn definidos no gateway no Azure com base no Nome do Gateway e no Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e9d4d-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="e9d4d-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9d4d-108">EXAMPLES</span></span>

### <span data-ttu-id="e9d4d-109">Exemplo 1: obtém os parâmetros Ipsec vpn definidos no Gateway de Rede Virtual para conexões ponto a site.</span><span class="sxs-lookup"><span data-stu-id="e9d4d-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="e9d4d-110">Retorna o objeto dos parâmetros ipsec vpn definidos no Gateway de Rede Virtual com o nome "myGateway" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="e9d4d-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="e9d4d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9d4d-111">PARAMETERS</span></span>

### <span data-ttu-id="e9d4d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d4d-112">-DefaultProfile</span></span>
<span data-ttu-id="e9d4d-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d4d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9d4d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9d4d-114">-Name</span></span>
<span data-ttu-id="e9d4d-115">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e9d4d-115">The resource name.</span></span>

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

### <span data-ttu-id="e9d4d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d4d-116">-ResourceGroupName</span></span>
<span data-ttu-id="e9d4d-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9d4d-117">The resource group name.</span></span>

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

### <span data-ttu-id="e9d4d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d4d-118">CommonParameters</span></span>
<span data-ttu-id="e9d4d-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d4d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d4d-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9d4d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d4d-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="e9d4d-121">INPUTS</span></span>

### <span data-ttu-id="e9d4d-122">System.String</span><span class="sxs-lookup"><span data-stu-id="e9d4d-122">System.String</span></span>

## <span data-ttu-id="e9d4d-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="e9d4d-123">OUTPUTS</span></span>

### <span data-ttu-id="e9d4d-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="e9d4d-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="e9d4d-125">Notas</span><span class="sxs-lookup"><span data-stu-id="e9d4d-125">NOTES</span></span>

## <span data-ttu-id="e9d4d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9d4d-126">RELATED LINKS</span></span>

[<span data-ttu-id="e9d4d-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e9d4d-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="e9d4d-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e9d4d-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="e9d4d-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e9d4d-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
