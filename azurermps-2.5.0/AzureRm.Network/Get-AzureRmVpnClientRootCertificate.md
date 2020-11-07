---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 7c3ee4e2c640417a7ba3d6cd78c2c8ea0691fff3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785691"
---
# <span data-ttu-id="2a789-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2a789-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="2a789-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a789-102">SYNOPSIS</span></span>
<span data-ttu-id="2a789-103">Obtém informações sobre certificados raiz VPN.</span><span class="sxs-lookup"><span data-stu-id="2a789-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a789-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a789-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a789-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a789-105">DESCRIPTION</span></span>
<span data-ttu-id="2a789-106">O cmdlet **Get-AzureRmVpnClientRootCertificate** retorna informações sobre os certificados raiz atribuídos a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2a789-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="2a789-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="2a789-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="2a789-108">Por padrão, **Get-AzureRmVpnClientRootCertificate** retorna informações sobre todos os certificados raiz atribuídos a um gateway.</span><span class="sxs-lookup"><span data-stu-id="2a789-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="2a789-109">(Os gateways podem ter mais de um certificado raiz.) No entanto, ao incluir o parâmetro **VpnClientRootCertificateName** , você pode limitar os dados retornados a um certificado específico.</span><span class="sxs-lookup"><span data-stu-id="2a789-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="2a789-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a789-110">EXAMPLES</span></span>

### <span data-ttu-id="2a789-111">Exemplo 1: obter informações sobre todos os certificados raiz</span><span class="sxs-lookup"><span data-stu-id="2a789-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="2a789-112">Esse comando obtém informações sobre todos os certificados raiz atribuídos a um gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="2a789-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="2a789-113">Exemplo 2: obter informações sobre certificados raiz específicos</span><span class="sxs-lookup"><span data-stu-id="2a789-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="2a789-114">Esse comando é uma variação do comando mostrado no exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="2a789-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="2a789-115">Nesse caso, no entanto, o parâmetro *VpnClientRootCertificateName* está incluído para limitar os dados retornados a um certificado raiz específico: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="2a789-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="2a789-116">OS</span><span class="sxs-lookup"><span data-stu-id="2a789-116">PARAMETERS</span></span>

### <span data-ttu-id="2a789-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a789-117">-DefaultProfile</span></span>
<span data-ttu-id="2a789-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a789-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a789-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a789-119">-ResourceGroupName</span></span>
<span data-ttu-id="2a789-120">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="2a789-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="2a789-121">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a789-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="2a789-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="2a789-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="2a789-123">Especifica o nome do gateway de rede virtual onde o certificado raiz está atribuído.</span><span class="sxs-lookup"><span data-stu-id="2a789-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="2a789-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="2a789-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="2a789-125">Especifica o nome do certificado raiz do cliente que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2a789-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a789-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a789-126">CommonParameters</span></span>
<span data-ttu-id="2a789-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a789-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a789-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a789-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a789-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a789-129">INPUTS</span></span>

## <span data-ttu-id="2a789-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a789-130">OUTPUTS</span></span>

###  
<span data-ttu-id="2a789-131">**Get-AzureRmVpnClientRootCertificate** Obtém instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="2a789-131">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="2a789-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a789-132">NOTES</span></span>

## <span data-ttu-id="2a789-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a789-133">RELATED LINKS</span></span>

[<span data-ttu-id="2a789-134">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2a789-134">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="2a789-135">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2a789-135">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="2a789-136">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2a789-136">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


