---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 4a34899a4e6c37ad3d4c84c173d07012110dcad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889771"
---
# <span data-ttu-id="56fe4-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fe4-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="56fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="56fe4-103">Cria uma Configuração de Ip a ser associada à Configuração do PrivateLink</span><span class="sxs-lookup"><span data-stu-id="56fe4-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="56fe4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="56fe4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56fe4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="56fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="56fe4-106">O cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** cria uma Configuração de Ip a ser associada à Configuração do PrivateLink para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="56fe4-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="56fe4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56fe4-107">EXAMPLES</span></span>

### <span data-ttu-id="56fe4-108">Exemplo 1: Configuração ip do PrivateLink</span><span class="sxs-lookup"><span data-stu-id="56fe4-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="56fe4-109">Este comando cria uma Configuração IP privateLink chamada 'ipConfig01' armazena o resultado na variável chamada $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="56fe4-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="56fe4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="56fe4-110">PARAMETERS</span></span>

### <span data-ttu-id="56fe4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fe4-111">-DefaultProfile</span></span>
<span data-ttu-id="56fe4-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56fe4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56fe4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="56fe4-113">-Name</span></span>
<span data-ttu-id="56fe4-114">O nome do IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fe4-114">The name of the IpConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56fe4-115">-Primary</span><span class="sxs-lookup"><span data-stu-id="56fe4-115">-Primary</span></span>
<span data-ttu-id="56fe4-116">Indica que a configuração ip é primária.</span><span class="sxs-lookup"><span data-stu-id="56fe4-116">Indicate the ip configuration is primary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56fe4-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="56fe4-117">-PrivateIpAddress</span></span>
<span data-ttu-id="56fe4-118">O endereço ip privado do ipConfiguration se a alocação estática for desejada.</span><span class="sxs-lookup"><span data-stu-id="56fe4-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56fe4-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="56fe4-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="56fe4-120">A versão ip da configuração ip</span><span class="sxs-lookup"><span data-stu-id="56fe4-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56fe4-121">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="56fe4-121">-Subnet</span></span>
<span data-ttu-id="56fe4-122">Sub-rede</span><span class="sxs-lookup"><span data-stu-id="56fe4-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56fe4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fe4-123">CommonParameters</span></span>
<span data-ttu-id="56fe4-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56fe4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fe4-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56fe4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fe4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56fe4-126">INPUTS</span></span>

### <span data-ttu-id="56fe4-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="56fe4-127">None</span></span>

## <span data-ttu-id="56fe4-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="56fe4-128">OUTPUTS</span></span>

### <span data-ttu-id="56fe4-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fe4-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="56fe4-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="56fe4-130">NOTES</span></span>

## <span data-ttu-id="56fe4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56fe4-131">RELATED LINKS</span></span>

[<span data-ttu-id="56fe4-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fe4-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
