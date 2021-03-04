---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: b952033bc6f04f2ed1e6d2e257dc68da1a6ec6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888847"
---
# <span data-ttu-id="bb752-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bb752-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="bb752-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb752-102">SYNOPSIS</span></span>
<span data-ttu-id="bb752-103">Adiciona um certificado de revogação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="bb752-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="bb752-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb752-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb752-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb752-105">DESCRIPTION</span></span>
<span data-ttu-id="bb752-106">O cmdlet **Add-AzVpnClientRevokedCertificate** atribui um certificado de revogação de cliente a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="bb752-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="bb752-107">Certificados de revogação de cliente impedem que os computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="bb752-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="bb752-108">Você precisa especificar o nome do certificado e a impressão digital do certificado para usar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb752-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="bb752-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb752-109">EXAMPLES</span></span>

### <span data-ttu-id="bb752-110">Exemplo 1: Adicionar um novo certificado de revogação de cliente a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="bb752-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="bb752-111">Este comando adiciona um novo certificado de revogação de cliente ao gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="bb752-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="bb752-112">Para adicionar o certificado, você deve especificar o nome do certificado e a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="bb752-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="bb752-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb752-113">PARAMETERS</span></span>

### <span data-ttu-id="bb752-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb752-114">-DefaultProfile</span></span>
<span data-ttu-id="bb752-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bb752-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb752-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb752-116">-ResourceGroupName</span></span>
<span data-ttu-id="bb752-117">Especifica o nome do grupo de recursos ao que o gateway de rede virtual é atribuído.</span><span class="sxs-lookup"><span data-stu-id="bb752-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="bb752-118">Os grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb752-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="bb752-119">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="bb752-119">-Thumbprint</span></span>
<span data-ttu-id="bb752-120">Especifica o identificador exclusivo do certificado que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="bb752-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="bb752-121">Por exemplo: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" Você pode obter informações de impressão digital para seus certificados usando um comando Windows PowerShell semelhante a este: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="bb752-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="bb752-122">O comando anterior obtém informações para todos os certificados de computador locais encontrados no armazenamento de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="bb752-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb752-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bb752-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bb752-124">Especifica o nome do gateway de rede virtual onde o certificado deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="bb752-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="bb752-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="bb752-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="bb752-126">Especifica o nome do certificado de cliente VPN a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="bb752-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="bb752-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb752-127">CommonParameters</span></span>
<span data-ttu-id="bb752-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb752-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb752-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb752-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb752-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb752-130">INPUTS</span></span>

### <span data-ttu-id="bb752-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bb752-131">System.String</span></span>

## <span data-ttu-id="bb752-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb752-132">OUTPUTS</span></span>

### <span data-ttu-id="bb752-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bb752-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="bb752-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb752-134">NOTES</span></span>

## <span data-ttu-id="bb752-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb752-135">RELATED LINKS</span></span>

[<span data-ttu-id="bb752-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bb752-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="bb752-137">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bb752-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="bb752-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bb752-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


