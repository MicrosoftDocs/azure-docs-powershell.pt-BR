---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428170"
---
# <span data-ttu-id="8b5b5-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8b5b5-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="8b5b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5b5-103">Adiciona um certificado de revogação do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="8b5b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b5b5-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b5b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b5b5-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5b5-106">O cmdlet **Add-AzVpnClientRevokedCertificate** atribui um certificado de revogação de cliente a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="8b5b5-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="8b5b5-108">Você precisa especificar o nome do certificado e a impressão digital do certificado para usar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="8b5b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b5b5-109">EXAMPLES</span></span>

### <span data-ttu-id="8b5b5-110">Exemplo 1: adicionar um novo certificado de revogação de cliente a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="8b5b5-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="8b5b5-111">Esse comando adiciona um novo certificado de revogação de cliente ao gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="8b5b5-112">Para adicionar o certificado, você deve especificar o nome do certificado e a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="8b5b5-113">OS</span><span class="sxs-lookup"><span data-stu-id="8b5b5-113">PARAMETERS</span></span>

### <span data-ttu-id="8b5b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5b5-114">-DefaultProfile</span></span>
<span data-ttu-id="8b5b5-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b5b5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b5b5-116">-ResourceGroupName</span></span>
<span data-ttu-id="8b5b5-117">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="8b5b5-118">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="8b5b5-119">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="8b5b5-119">-Thumbprint</span></span>
<span data-ttu-id="8b5b5-120">Especifica o identificador exclusivo do certificado que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="8b5b5-121">Por exemplo:-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" você pode obter informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="8b5b5-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="8b5b5-122">O comando anterior obtém informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="8b5b5-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8b5b5-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8b5b5-124">Especifica o nome do gateway de rede virtual onde o certificado deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="8b5b5-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="8b5b5-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="8b5b5-126">Especifica o nome do certificado de cliente VPN a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="8b5b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5b5-127">CommonParameters</span></span>
<span data-ttu-id="8b5b5-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5b5-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b5b5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5b5-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b5b5-130">INPUTS</span></span>

### <span data-ttu-id="8b5b5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8b5b5-131">System.String</span></span>

## <span data-ttu-id="8b5b5-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b5b5-132">OUTPUTS</span></span>

### <span data-ttu-id="8b5b5-133">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8b5b5-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="8b5b5-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b5b5-134">NOTES</span></span>

## <span data-ttu-id="8b5b5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b5b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="8b5b5-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8b5b5-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="8b5b5-137">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8b5b5-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="8b5b5-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8b5b5-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


