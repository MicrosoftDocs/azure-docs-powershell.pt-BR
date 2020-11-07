---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: 62fc89cefadc91445a64850d6a0e5ee23d6163f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785693"
---
# <span data-ttu-id="061c7-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="061c7-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="061c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="061c7-102">SYNOPSIS</span></span>
<span data-ttu-id="061c7-103">Obtém informações sobre o cliente VPN-certificados de revogação.</span><span class="sxs-lookup"><span data-stu-id="061c7-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="061c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="061c7-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="061c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="061c7-105">DESCRIPTION</span></span>
<span data-ttu-id="061c7-106">O cmdlet **Get-AzureRmVpnClientRevokedCertificate** retorna informações sobre os certificados de revogação de cliente atribuídos a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="061c7-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="061c7-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="061c7-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="061c7-108">**Get-AzureRmVpnClientRevokedCertificate** permite retornar informações sobre todos os certificados de revogação de cliente no gateway ou usando o parâmetro *VpnClientRevokedCertificateName* para obter informações sobre um único certificado.</span><span class="sxs-lookup"><span data-stu-id="061c7-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="061c7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="061c7-109">EXAMPLES</span></span>

### <span data-ttu-id="061c7-110">Exemplo 1: obter informações sobre todos os certificados de revogação de cliente</span><span class="sxs-lookup"><span data-stu-id="061c7-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="061c7-111">Esse comando obtém informações sobre todos os certificados de revogação de cliente associados ao gateway de rede virtual chamado ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="061c7-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="061c7-112">Exemplo 2: obter informações sobre certificados de revogação do cliente específico</span><span class="sxs-lookup"><span data-stu-id="061c7-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="061c7-113">Esse comando é uma variação do comando mostrado no exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="061c7-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="061c7-114">Nesse caso, no entanto, o parâmetro *VpnClientRevokedCertificateName* é usado para limitar os dados retornados a um certificado revogado pelo cliente específico: o certificado com o nome ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="061c7-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="061c7-115">OS</span><span class="sxs-lookup"><span data-stu-id="061c7-115">PARAMETERS</span></span>

### <span data-ttu-id="061c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="061c7-116">-DefaultProfile</span></span>
<span data-ttu-id="061c7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="061c7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="061c7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="061c7-118">-ResourceGroupName</span></span>
<span data-ttu-id="061c7-119">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="061c7-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="061c7-120">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="061c7-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="061c7-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="061c7-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="061c7-122">Especifica o nome do gateway de rede virtual onde as informações de certificado revogado são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="061c7-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="061c7-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="061c7-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="061c7-124">Especifica o nome do certificado de cliente VPN que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="061c7-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="061c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="061c7-125">CommonParameters</span></span>
<span data-ttu-id="061c7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="061c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="061c7-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="061c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="061c7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="061c7-128">INPUTS</span></span>

## <span data-ttu-id="061c7-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="061c7-129">OUTPUTS</span></span>

###  
<span data-ttu-id="061c7-130">**Get-AzureRmVpnClientRevokedCertificate** retorna instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="061c7-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="061c7-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="061c7-131">NOTES</span></span>

## <span data-ttu-id="061c7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="061c7-132">RELATED LINKS</span></span>

[<span data-ttu-id="061c7-133">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="061c7-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="061c7-134">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="061c7-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="061c7-135">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="061c7-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


