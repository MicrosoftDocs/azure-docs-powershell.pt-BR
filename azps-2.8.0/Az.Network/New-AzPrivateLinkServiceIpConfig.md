---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: c7ea999af626206b741e86457d92627e4db196a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771598"
---
# <span data-ttu-id="192d5-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="192d5-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="192d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="192d5-102">SYNOPSIS</span></span>
<span data-ttu-id="192d5-103">Crie uma configuração de IP do serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="192d5-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="192d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="192d5-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="192d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="192d5-105">DESCRIPTION</span></span>
<span data-ttu-id="192d5-106">O cmdlet **New-AzPrivateLinkServiceIpConfig** cria uma configuração de IP de serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="192d5-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="192d5-107">Essa configuração é usada para o NAT de origem do tráfego de entrada do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="192d5-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="192d5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="192d5-108">EXAMPLES</span></span>

### <span data-ttu-id="192d5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="192d5-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="192d5-110">Este exemplo cria uma configuração de IP do serviço de link privado na memória.</span><span class="sxs-lookup"><span data-stu-id="192d5-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="192d5-111">OS</span><span class="sxs-lookup"><span data-stu-id="192d5-111">PARAMETERS</span></span>

### <span data-ttu-id="192d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192d5-112">-DefaultProfile</span></span>
<span data-ttu-id="192d5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="192d5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="192d5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="192d5-114">-Name</span></span>
<span data-ttu-id="192d5-115">O nome da IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="192d5-115">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="192d5-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="192d5-116">-PrivateIpAddress</span></span>
<span data-ttu-id="192d5-117">O endereço IP privado da ipConfiguration se a alocação estática for especificada.</span><span class="sxs-lookup"><span data-stu-id="192d5-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

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

### <span data-ttu-id="192d5-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="192d5-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="192d5-119">A versão de IP da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="192d5-119">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="192d5-120">-Principal</span><span class="sxs-lookup"><span data-stu-id="192d5-120">-Primary</span></span>
<span data-ttu-id="192d5-121">Indicar que a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="192d5-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="192d5-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="192d5-122">-Subnet</span></span>
<span data-ttu-id="192d5-123">Redes</span><span class="sxs-lookup"><span data-stu-id="192d5-123">Subnet</span></span>

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

### <span data-ttu-id="192d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192d5-124">CommonParameters</span></span>
<span data-ttu-id="192d5-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="192d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192d5-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="192d5-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192d5-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="192d5-127">INPUTS</span></span>

### <span data-ttu-id="192d5-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="192d5-128">None</span></span>

## <span data-ttu-id="192d5-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="192d5-129">OUTPUTS</span></span>

### <span data-ttu-id="192d5-130">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="192d5-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="192d5-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="192d5-131">NOTES</span></span>

## <span data-ttu-id="192d5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="192d5-132">RELATED LINKS</span></span>

[<span data-ttu-id="192d5-133">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="192d5-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)