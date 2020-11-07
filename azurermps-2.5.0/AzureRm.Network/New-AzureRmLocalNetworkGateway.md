---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: c450d2f6fd3d9a9b0368a667573aadadbd218d8f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785908"
---
# <span data-ttu-id="318f6-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="318f6-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="318f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="318f6-102">SYNOPSIS</span></span>
<span data-ttu-id="318f6-103">Cria um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="318f6-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="318f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="318f6-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="318f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="318f6-105">DESCRIPTION</span></span>
<span data-ttu-id="318f6-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="318f6-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="318f6-107">O cmdlet **New-AzureRmLocalNetworkGateway** cria o objeto que representa o gateway local de acordo com o nome, o nome do grupo de recursos, o local e o endereço IP do gateway, bem como o prefixo do endereço da rede local que será conectada ao Azure.</span><span class="sxs-lookup"><span data-stu-id="318f6-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="318f6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="318f6-108">EXAMPLES</span></span>

### <span data-ttu-id="318f6-109">1: criar um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="318f6-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="318f6-110">Cria o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG" no local "West US" com o endereço IP "23.99.221.164" e o prefixo de endereço "10.5.51.0/24" local.</span><span class="sxs-lookup"><span data-stu-id="318f6-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="318f6-111">OS</span><span class="sxs-lookup"><span data-stu-id="318f6-111">PARAMETERS</span></span>

### <span data-ttu-id="318f6-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="318f6-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="318f6-113">-AsJob</span></span>
<span data-ttu-id="318f6-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="318f6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="318f6-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="318f6-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="318f6-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318f6-117">-DefaultProfile</span></span>
<span data-ttu-id="318f6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="318f6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="318f6-119">-Force</span></span>
<span data-ttu-id="318f6-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="318f6-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="318f6-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="318f6-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-122">-Local</span><span class="sxs-lookup"><span data-stu-id="318f6-122">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="318f6-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="318f6-124">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="318f6-126">Especifica o grupo de recursos ao qual pertence o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="318f6-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="318f6-127">-Tag</span></span>
<span data-ttu-id="318f6-128">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="318f6-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="318f6-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="318f6-129">For example:</span></span>

<span data-ttu-id="318f6-130">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="318f6-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="318f6-131">-Confirm</span></span>
<span data-ttu-id="318f6-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="318f6-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318f6-133">-WhatIf</span></span>
<span data-ttu-id="318f6-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="318f6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="318f6-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="318f6-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318f6-136">CommonParameters</span></span>
<span data-ttu-id="318f6-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318f6-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318f6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318f6-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="318f6-139">INPUTS</span></span>

## <span data-ttu-id="318f6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="318f6-140">OUTPUTS</span></span>

### <span data-ttu-id="318f6-141">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="318f6-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="318f6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="318f6-142">NOTES</span></span>

## <span data-ttu-id="318f6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="318f6-143">RELATED LINKS</span></span>

[<span data-ttu-id="318f6-144">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="318f6-144">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="318f6-145">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="318f6-145">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="318f6-146">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="318f6-146">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
