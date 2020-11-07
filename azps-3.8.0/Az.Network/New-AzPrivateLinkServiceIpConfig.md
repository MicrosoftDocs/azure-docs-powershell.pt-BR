---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: e1d7c2d78bf58240cc87e7a224be1632828984d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943257"
---
# <span data-ttu-id="9202b-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9202b-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="9202b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9202b-102">SYNOPSIS</span></span>
<span data-ttu-id="9202b-103">Crie uma configuração de IP do serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="9202b-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="9202b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9202b-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9202b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9202b-105">DESCRIPTION</span></span>
<span data-ttu-id="9202b-106">O cmdlet **New-AzPrivateLinkServiceIpConfig** cria uma configuração de IP de serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="9202b-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="9202b-107">Essa configuração é usada para o NAT de origem do tráfego de entrada do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="9202b-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="9202b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9202b-108">EXAMPLES</span></span>

### <span data-ttu-id="9202b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9202b-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="9202b-110">Este exemplo cria uma configuração de IP do serviço de link privado na memória.</span><span class="sxs-lookup"><span data-stu-id="9202b-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="9202b-111">OS</span><span class="sxs-lookup"><span data-stu-id="9202b-111">PARAMETERS</span></span>

### <span data-ttu-id="9202b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9202b-112">-DefaultProfile</span></span>
<span data-ttu-id="9202b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9202b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9202b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="9202b-114">-Name</span></span>
<span data-ttu-id="9202b-115">O nome da IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9202b-115">The name of the IpConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9202b-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9202b-116">-PrivateIpAddress</span></span>
<span data-ttu-id="9202b-117">O endereço IP privado da ipConfiguration se a alocação estática for especificada.</span><span class="sxs-lookup"><span data-stu-id="9202b-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9202b-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9202b-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="9202b-119">A versão de IP da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="9202b-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9202b-120">-Principal</span><span class="sxs-lookup"><span data-stu-id="9202b-120">-Primary</span></span>
<span data-ttu-id="9202b-121">Indicar que a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="9202b-121">Indicate current ip configuration is primary or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9202b-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="9202b-122">-Subnet</span></span>
<span data-ttu-id="9202b-123">Redes</span><span class="sxs-lookup"><span data-stu-id="9202b-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9202b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9202b-124">CommonParameters</span></span>
<span data-ttu-id="9202b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9202b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9202b-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9202b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9202b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9202b-127">INPUTS</span></span>

### <span data-ttu-id="9202b-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9202b-128">None</span></span>

## <span data-ttu-id="9202b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9202b-129">OUTPUTS</span></span>

### <span data-ttu-id="9202b-130">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9202b-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="9202b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9202b-131">NOTES</span></span>

## <span data-ttu-id="9202b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9202b-132">RELATED LINKS</span></span>

[<span data-ttu-id="9202b-133">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9202b-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)