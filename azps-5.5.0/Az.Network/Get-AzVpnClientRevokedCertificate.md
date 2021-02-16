---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113493"
---
# <span data-ttu-id="30c34-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="30c34-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="30c34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30c34-102">SYNOPSIS</span></span>
<span data-ttu-id="30c34-103">Obtém informações sobre certificados de revogação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="30c34-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="30c34-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30c34-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30c34-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="30c34-105">DESCRIPTION</span></span>
<span data-ttu-id="30c34-106">O cmdlet **Get-AzVpnClientRevokedCertificate** retorna informações sobre os certificados de revogação de cliente atribuídos a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="30c34-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="30c34-107">Certificados de revogação de cliente impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="30c34-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="30c34-108">O **Get-AzVpnClientRevokedCertificate** permite que você retorne informações sobre todos os certificados revogados pelo cliente no gateway ou, usando o parâmetro *VpnClientRevokedCertificateName,* para obter informações sobre um único certificado.</span><span class="sxs-lookup"><span data-stu-id="30c34-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="30c34-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30c34-109">EXAMPLES</span></span>

### <span data-ttu-id="30c34-110">Exemplo 1: obter informações sobre todos os certificados revogados pelo cliente</span><span class="sxs-lookup"><span data-stu-id="30c34-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="30c34-111">Esse comando obtém informações sobre todos os certificados de revogação de cliente associados ao gateway de rede virtual chamado ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="30c34-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="30c34-112">Exemplo 2: obter informações sobre certificados de revogação de cliente específicos</span><span class="sxs-lookup"><span data-stu-id="30c34-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="30c34-113">Este comando é uma variação do comando mostrado no Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="30c34-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="30c34-114">Nesse caso, no entanto, o parâmetro *VpnClientRevokedCertificateName* é usado para limitar os dados retornados a um certificado revogado por cliente específico: o certificado com o nome ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="30c34-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="30c34-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30c34-115">PARAMETERS</span></span>

### <span data-ttu-id="30c34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c34-116">-DefaultProfile</span></span>
<span data-ttu-id="30c34-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="30c34-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c34-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c34-118">-ResourceGroupName</span></span>
<span data-ttu-id="30c34-119">Especifica o nome do grupo de recursos ao que o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="30c34-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="30c34-120">Os grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de estoque e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="30c34-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="30c34-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="30c34-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="30c34-122">Especifica o nome do gateway de rede virtual onde as informações de certificado revogadas são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="30c34-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="30c34-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="30c34-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="30c34-124">Especifica o nome do certificado do cliente VPN que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="30c34-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="30c34-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c34-125">CommonParameters</span></span>
<span data-ttu-id="30c34-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c34-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c34-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30c34-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c34-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="30c34-128">INPUTS</span></span>

### <span data-ttu-id="30c34-129">System.String</span><span class="sxs-lookup"><span data-stu-id="30c34-129">System.String</span></span>

## <span data-ttu-id="30c34-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="30c34-130">OUTPUTS</span></span>

### <span data-ttu-id="30c34-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="30c34-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="30c34-132">Notas</span><span class="sxs-lookup"><span data-stu-id="30c34-132">NOTES</span></span>

## <span data-ttu-id="30c34-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30c34-133">RELATED LINKS</span></span>

[<span data-ttu-id="30c34-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="30c34-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="30c34-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="30c34-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="30c34-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="30c34-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


