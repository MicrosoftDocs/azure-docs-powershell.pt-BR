---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: c5ceef5ec70ac337180c8e2fcf6bb567c68391a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885412"
---
# <span data-ttu-id="a7676-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a7676-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a7676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7676-102">SYNOPSIS</span></span>
<span data-ttu-id="a7676-103">Obtém informações sobre certificados de revogação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="a7676-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="a7676-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a7676-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7676-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7676-105">DESCRIPTION</span></span>
<span data-ttu-id="a7676-106">O cmdlet **Get-AzVpnClientRevokedCertificate** retorna informações sobre os certificados de revogação do cliente atribuídos a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a7676-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="a7676-107">Certificados de revogação de cliente impedem que os computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="a7676-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="a7676-108">**Get-AzVpnClientRevokedCertificate** permite que você retorne informações sobre todos os certificados de revogação do cliente no gateway ou, usando o *parâmetro VpnClientRevokedCertificateName,* para obter informações sobre um único certificado.</span><span class="sxs-lookup"><span data-stu-id="a7676-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="a7676-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7676-109">EXAMPLES</span></span>

### <span data-ttu-id="a7676-110">Exemplo 1: obter informações sobre todos os certificados de revogação do cliente</span><span class="sxs-lookup"><span data-stu-id="a7676-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="a7676-111">Este comando obtém informações sobre todos os certificados de revogação do cliente associados ao gateway de rede virtual chamado ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a7676-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="a7676-112">Exemplo 2: obter informações sobre certificados de revogação de cliente específicos</span><span class="sxs-lookup"><span data-stu-id="a7676-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="a7676-113">Este comando é uma variação do comando mostrado no Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="a7676-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="a7676-114">Nesse caso, no entanto, o *parâmetro VpnClientRevokedCertificateName* é usado para limitar os dados retornados a um certificado revogado por cliente específico: o certificado com o nome ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="a7676-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="a7676-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a7676-115">PARAMETERS</span></span>

### <span data-ttu-id="a7676-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7676-116">-DefaultProfile</span></span>
<span data-ttu-id="a7676-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a7676-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7676-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7676-118">-ResourceGroupName</span></span>
<span data-ttu-id="a7676-119">Especifica o nome do grupo de recursos ao que o gateway de rede virtual é atribuído.</span><span class="sxs-lookup"><span data-stu-id="a7676-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="a7676-120">Os grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="a7676-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a7676-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a7676-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a7676-122">Especifica o nome do gateway de rede virtual no qual as informações de certificado revogadas são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="a7676-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="a7676-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="a7676-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="a7676-124">Especifica o nome do certificado de cliente VPN que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a7676-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7676-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7676-125">CommonParameters</span></span>
<span data-ttu-id="a7676-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7676-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7676-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7676-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7676-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7676-128">INPUTS</span></span>

### <span data-ttu-id="a7676-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a7676-129">System.String</span></span>

## <span data-ttu-id="a7676-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a7676-130">OUTPUTS</span></span>

### <span data-ttu-id="a7676-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a7676-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a7676-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="a7676-132">NOTES</span></span>

## <span data-ttu-id="a7676-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7676-133">RELATED LINKS</span></span>

[<span data-ttu-id="a7676-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a7676-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="a7676-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a7676-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="a7676-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a7676-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


