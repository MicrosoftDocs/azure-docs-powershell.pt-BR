---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: bec6ded02853fbcfc08db38f0e627433d1d1ae10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430147"
---
# <span data-ttu-id="23162-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23162-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="23162-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23162-102">SYNOPSIS</span></span>
<span data-ttu-id="23162-103">Cria um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="23162-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23162-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23162-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23162-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23162-105">DESCRIPTION</span></span>
<span data-ttu-id="23162-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="23162-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="23162-107">O cmdlet **New-AzureRmLocalNetworkGateway** cria o objeto que representa o gateway local de acordo com o nome, o nome do grupo de recursos, o local e o endereço IP do gateway, bem como o prefixo do endereço da rede local que será conectada ao Azure.</span><span class="sxs-lookup"><span data-stu-id="23162-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="23162-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23162-108">EXAMPLES</span></span>

### <span data-ttu-id="23162-109">1: criar um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="23162-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="23162-110">Cria o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG" no local "West US" com o endereço IP "23.99.221.164" e o prefixo de endereço "10.5.51.0/24" local.</span><span class="sxs-lookup"><span data-stu-id="23162-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="23162-111">OS</span><span class="sxs-lookup"><span data-stu-id="23162-111">PARAMETERS</span></span>

### <span data-ttu-id="23162-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="23162-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="23162-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23162-113">-AsJob</span></span>
<span data-ttu-id="23162-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="23162-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23162-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="23162-115">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23162-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="23162-116">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23162-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23162-117">-DefaultProfile</span></span>
<span data-ttu-id="23162-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23162-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23162-119">-Force</span><span class="sxs-lookup"><span data-stu-id="23162-119">-Force</span></span>
<span data-ttu-id="23162-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="23162-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23162-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="23162-121">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23162-122">-Local</span><span class="sxs-lookup"><span data-stu-id="23162-122">-Location</span></span>
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

### <span data-ttu-id="23162-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="23162-123">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23162-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="23162-124">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23162-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23162-125">-ResourceGroupName</span></span>
<span data-ttu-id="23162-126">Especifica o grupo de recursos ao qual pertence o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="23162-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="23162-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="23162-127">-Tag</span></span>
<span data-ttu-id="23162-128">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="23162-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="23162-129">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="23162-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23162-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23162-130">-Confirm</span></span>
<span data-ttu-id="23162-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23162-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23162-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23162-132">-WhatIf</span></span>
<span data-ttu-id="23162-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23162-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23162-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23162-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23162-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23162-135">CommonParameters</span></span>
<span data-ttu-id="23162-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23162-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23162-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23162-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23162-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23162-138">INPUTS</span></span>

### <span data-ttu-id="23162-139">System. String</span><span class="sxs-lookup"><span data-stu-id="23162-139">System.String</span></span>

### <span data-ttu-id="23162-140">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="23162-140">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="23162-141">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="23162-141">System.UInt32</span></span>

### <span data-ttu-id="23162-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="23162-142">System.Int32</span></span>

### <span data-ttu-id="23162-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="23162-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="23162-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23162-144">OUTPUTS</span></span>

### <span data-ttu-id="23162-145">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23162-145">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="23162-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23162-146">NOTES</span></span>

## <span data-ttu-id="23162-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23162-147">RELATED LINKS</span></span>

[<span data-ttu-id="23162-148">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23162-148">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="23162-149">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23162-149">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="23162-150">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23162-150">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
