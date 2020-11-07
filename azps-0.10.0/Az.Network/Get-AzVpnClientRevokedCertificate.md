---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 3151ffb45064d1cb85b69d11a1ccbd49d4c045e8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775449"
---
# <span data-ttu-id="02d63-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="02d63-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="02d63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02d63-102">SYNOPSIS</span></span>
<span data-ttu-id="02d63-103">Obtém informações sobre o cliente VPN-certificados de revogação.</span><span class="sxs-lookup"><span data-stu-id="02d63-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="02d63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02d63-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02d63-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02d63-105">DESCRIPTION</span></span>
<span data-ttu-id="02d63-106">O cmdlet **Get-AzVpnClientRevokedCertificate** retorna informações sobre os certificados de revogação de cliente atribuídos a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="02d63-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="02d63-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="02d63-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="02d63-108">**Get-AzVpnClientRevokedCertificate** permite retornar informações sobre todos os certificados de revogação de cliente no gateway ou usando o parâmetro *VpnClientRevokedCertificateName* para obter informações sobre um único certificado.</span><span class="sxs-lookup"><span data-stu-id="02d63-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="02d63-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02d63-109">EXAMPLES</span></span>

### <span data-ttu-id="02d63-110">Exemplo 1: obter informações sobre todos os certificados de revogação de cliente</span><span class="sxs-lookup"><span data-stu-id="02d63-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="02d63-111">Esse comando obtém informações sobre todos os certificados de revogação de cliente associados ao gateway de rede virtual chamado ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="02d63-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="02d63-112">Exemplo 2: obter informações sobre certificados de revogação do cliente específico</span><span class="sxs-lookup"><span data-stu-id="02d63-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="02d63-113">Esse comando é uma variação do comando mostrado no exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="02d63-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="02d63-114">Nesse caso, no entanto, o parâmetro *VpnClientRevokedCertificateName* é usado para limitar os dados retornados a um certificado revogado pelo cliente específico: o certificado com o nome ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="02d63-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="02d63-115">OS</span><span class="sxs-lookup"><span data-stu-id="02d63-115">PARAMETERS</span></span>

### <span data-ttu-id="02d63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d63-116">-DefaultProfile</span></span>
<span data-ttu-id="02d63-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02d63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d63-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d63-118">-ResourceGroupName</span></span>
<span data-ttu-id="02d63-119">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="02d63-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="02d63-120">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="02d63-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="02d63-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="02d63-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="02d63-122">Especifica o nome do gateway de rede virtual onde as informações de certificado revogado são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="02d63-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="02d63-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="02d63-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="02d63-124">Especifica o nome do certificado de cliente VPN que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="02d63-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="02d63-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d63-125">CommonParameters</span></span>
<span data-ttu-id="02d63-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d63-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d63-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d63-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d63-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02d63-128">INPUTS</span></span>

## <span data-ttu-id="02d63-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02d63-129">OUTPUTS</span></span>

###  
<span data-ttu-id="02d63-130">**Get-AzVpnClientRevokedCertificate** retorna instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="02d63-130">**Get-AzVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="02d63-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02d63-131">NOTES</span></span>

## <span data-ttu-id="02d63-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02d63-132">RELATED LINKS</span></span>

[<span data-ttu-id="02d63-133">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="02d63-133">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="02d63-134">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="02d63-134">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="02d63-135">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="02d63-135">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


