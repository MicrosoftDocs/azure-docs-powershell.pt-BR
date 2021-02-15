---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117414"
---
# <span data-ttu-id="93a03-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a03-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="93a03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93a03-102">SYNOPSIS</span></span>
<span data-ttu-id="93a03-103">Cria uma Configuração Ip a ser associada à Configuração do PrivateLink</span><span class="sxs-lookup"><span data-stu-id="93a03-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="93a03-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93a03-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93a03-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="93a03-105">DESCRIPTION</span></span>
<span data-ttu-id="93a03-106">O cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** cria uma Configuração Ip a ser associada à Configuração do PrivateLink para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="93a03-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="93a03-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="93a03-107">EXAMPLES</span></span>

### <span data-ttu-id="93a03-108">Exemplo 1: Configuração ip do PrivateLink</span><span class="sxs-lookup"><span data-stu-id="93a03-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="93a03-109">Esse comando cria uma Configuração IP do PrivateLink chamada 'ipConfig01' armazena o resultado na variável chamada $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="93a03-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="93a03-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93a03-110">PARAMETERS</span></span>

### <span data-ttu-id="93a03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a03-111">-DefaultProfile</span></span>
<span data-ttu-id="93a03-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93a03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93a03-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="93a03-113">-Name</span></span>
<span data-ttu-id="93a03-114">O nome da Configuração IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a03-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="93a03-115">-Principal</span><span class="sxs-lookup"><span data-stu-id="93a03-115">-Primary</span></span>
<span data-ttu-id="93a03-116">Indique que a configuração de ip é primária.</span><span class="sxs-lookup"><span data-stu-id="93a03-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="93a03-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="93a03-117">-PrivateIpAddress</span></span>
<span data-ttu-id="93a03-118">O endereço ip particular da ipConfiguration se a alocação estática for desejada.</span><span class="sxs-lookup"><span data-stu-id="93a03-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="93a03-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="93a03-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="93a03-120">A versão ip da configuração ip</span><span class="sxs-lookup"><span data-stu-id="93a03-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="93a03-121">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="93a03-121">-Subnet</span></span>
<span data-ttu-id="93a03-122">Sub-rede</span><span class="sxs-lookup"><span data-stu-id="93a03-122">Subnet</span></span>

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

### <span data-ttu-id="93a03-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a03-123">CommonParameters</span></span>
<span data-ttu-id="93a03-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a03-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a03-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93a03-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a03-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="93a03-126">INPUTS</span></span>

### <span data-ttu-id="93a03-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93a03-127">None</span></span>

## <span data-ttu-id="93a03-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="93a03-128">OUTPUTS</span></span>

### <span data-ttu-id="93a03-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a03-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="93a03-130">Notas</span><span class="sxs-lookup"><span data-stu-id="93a03-130">NOTES</span></span>

## <span data-ttu-id="93a03-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93a03-131">RELATED LINKS</span></span>

[<span data-ttu-id="93a03-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a03-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
