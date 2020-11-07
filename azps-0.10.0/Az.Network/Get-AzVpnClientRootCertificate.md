---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: c55fb1af95b1c0f85e2b36732f6235ad0c6c78d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775447"
---
# <span data-ttu-id="c1b90-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1b90-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="c1b90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1b90-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b90-103">Obtém informações sobre certificados raiz VPN.</span><span class="sxs-lookup"><span data-stu-id="c1b90-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="c1b90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1b90-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1b90-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1b90-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b90-106">O cmdlet **Get-AzVpnClientRootCertificate** retorna informações sobre os certificados raiz atribuídos a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c1b90-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="c1b90-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="c1b90-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="c1b90-108">Por padrão, **Get-AzVpnClientRootCertificate** retorna informações sobre todos os certificados raiz atribuídos a um gateway.</span><span class="sxs-lookup"><span data-stu-id="c1b90-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="c1b90-109">(Os gateways podem ter mais de um certificado raiz.) No entanto, ao incluir o parâmetro **VpnClientRootCertificateName** , você pode limitar os dados retornados a um certificado específico.</span><span class="sxs-lookup"><span data-stu-id="c1b90-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="c1b90-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1b90-110">EXAMPLES</span></span>

### <span data-ttu-id="c1b90-111">Exemplo 1: obter informações sobre todos os certificados raiz</span><span class="sxs-lookup"><span data-stu-id="c1b90-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="c1b90-112">Esse comando obtém informações sobre todos os certificados raiz atribuídos a um gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="c1b90-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="c1b90-113">Exemplo 2: obter informações sobre certificados raiz específicos</span><span class="sxs-lookup"><span data-stu-id="c1b90-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="c1b90-114">Esse comando é uma variação do comando mostrado no exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c1b90-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="c1b90-115">Nesse caso, no entanto, o parâmetro *VpnClientRootCertificateName* está incluído para limitar os dados retornados a um certificado raiz específico: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="c1b90-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="c1b90-116">OS</span><span class="sxs-lookup"><span data-stu-id="c1b90-116">PARAMETERS</span></span>

### <span data-ttu-id="c1b90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b90-117">-DefaultProfile</span></span>
<span data-ttu-id="c1b90-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b90-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b90-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b90-119">-ResourceGroupName</span></span>
<span data-ttu-id="c1b90-120">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c1b90-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="c1b90-121">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b90-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="c1b90-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c1b90-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c1b90-123">Especifica o nome do gateway de rede virtual onde o certificado raiz está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c1b90-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="c1b90-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="c1b90-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="c1b90-125">Especifica o nome do certificado raiz do cliente que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c1b90-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c1b90-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b90-126">CommonParameters</span></span>
<span data-ttu-id="c1b90-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b90-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b90-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b90-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b90-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1b90-129">INPUTS</span></span>

## <span data-ttu-id="c1b90-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1b90-130">OUTPUTS</span></span>

###  
<span data-ttu-id="c1b90-131">**Get-AzVpnClientRootCertificate** Obtém instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="c1b90-131">**Get-AzVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="c1b90-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1b90-132">NOTES</span></span>

## <span data-ttu-id="c1b90-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1b90-133">RELATED LINKS</span></span>

[<span data-ttu-id="c1b90-134">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1b90-134">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="c1b90-135">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1b90-135">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="c1b90-136">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1b90-136">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)

