---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271780"
---
# <span data-ttu-id="74764-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="74764-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="74764-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74764-102">SYNOPSIS</span></span>
<span data-ttu-id="74764-103">Cria uma configuração de IP a ser associada à configuração do PrivateLink</span><span class="sxs-lookup"><span data-stu-id="74764-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="74764-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74764-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74764-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74764-105">DESCRIPTION</span></span>
<span data-ttu-id="74764-106">O cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** cria uma configuração de IP para ser associada à configuração do PrivateLink para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="74764-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="74764-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74764-107">EXAMPLES</span></span>

### <span data-ttu-id="74764-108">Exemplo 1: configuração de IP do PrivateLink</span><span class="sxs-lookup"><span data-stu-id="74764-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="74764-109">Esse comando cria uma configuração de IP PrivateLink chamada ' ipConfig01 ' que armazena o resultado na variável chamada $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="74764-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="74764-110">OS</span><span class="sxs-lookup"><span data-stu-id="74764-110">PARAMETERS</span></span>

### <span data-ttu-id="74764-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74764-111">-DefaultProfile</span></span>
<span data-ttu-id="74764-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74764-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74764-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="74764-113">-Name</span></span>
<span data-ttu-id="74764-114">O nome da IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="74764-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="74764-115">-Principal</span><span class="sxs-lookup"><span data-stu-id="74764-115">-Primary</span></span>
<span data-ttu-id="74764-116">Indicar que a configuração de IP é primária.</span><span class="sxs-lookup"><span data-stu-id="74764-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="74764-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="74764-117">-PrivateIpAddress</span></span>
<span data-ttu-id="74764-118">O endereço IP privado da ipConfiguration se desejar uma atribuição estática.</span><span class="sxs-lookup"><span data-stu-id="74764-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="74764-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="74764-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="74764-120">A versão de IP da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="74764-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="74764-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="74764-121">-Subnet</span></span>
<span data-ttu-id="74764-122">Redes</span><span class="sxs-lookup"><span data-stu-id="74764-122">Subnet</span></span>

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

### <span data-ttu-id="74764-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74764-123">CommonParameters</span></span>
<span data-ttu-id="74764-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74764-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74764-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74764-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74764-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74764-126">INPUTS</span></span>

### <span data-ttu-id="74764-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="74764-127">None</span></span>

## <span data-ttu-id="74764-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74764-128">OUTPUTS</span></span>

### <span data-ttu-id="74764-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="74764-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="74764-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74764-130">NOTES</span></span>

## <span data-ttu-id="74764-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74764-131">RELATED LINKS</span></span>

[<span data-ttu-id="74764-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="74764-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
