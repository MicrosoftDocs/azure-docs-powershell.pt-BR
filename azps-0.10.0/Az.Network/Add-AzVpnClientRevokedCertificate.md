---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 384d5b88ce9a52ad5f68c009c7b610610c695ce2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775607"
---
# <span data-ttu-id="6e129-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6e129-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="6e129-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e129-102">SYNOPSIS</span></span>
<span data-ttu-id="6e129-103">Adiciona um certificado de revogação do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="6e129-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="6e129-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e129-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e129-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e129-105">DESCRIPTION</span></span>
<span data-ttu-id="6e129-106">O cmdlet **Add-AzVpnClientRevokedCertificate** atribui um certificado de revogação de cliente a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6e129-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="6e129-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="6e129-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="6e129-108">Você precisa especificar o nome do certificado e a impressão digital do certificado para usar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e129-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="6e129-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e129-109">EXAMPLES</span></span>

### <span data-ttu-id="6e129-110">Exemplo 1: adicionar um novo certificado de revogação de cliente a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6e129-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="6e129-111">Esse comando adiciona um novo certificado de revogação de cliente ao gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="6e129-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="6e129-112">Para adicionar o certificado, você deve especificar o nome do certificado e a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="6e129-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="6e129-113">OS</span><span class="sxs-lookup"><span data-stu-id="6e129-113">PARAMETERS</span></span>

### <span data-ttu-id="6e129-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e129-114">-DefaultProfile</span></span>
<span data-ttu-id="6e129-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e129-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e129-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e129-116">-ResourceGroupName</span></span>
<span data-ttu-id="6e129-117">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="6e129-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="6e129-118">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e129-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="6e129-119">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="6e129-119">-Thumbprint</span></span>
<span data-ttu-id="6e129-120">Especifica o identificador exclusivo do certificado que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="6e129-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="6e129-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6e129-121">For example:</span></span>

<span data-ttu-id="6e129-122">-Impressão digital "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="6e129-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="6e129-123">Você pode obter informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="6e129-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="6e129-124">O comando anterior obtém informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="6e129-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e129-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="6e129-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="6e129-126">Especifica o nome do gateway de rede virtual onde o certificado deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="6e129-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="6e129-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="6e129-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="6e129-128">Especifica o nome do certificado de cliente VPN a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="6e129-128">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="6e129-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e129-129">CommonParameters</span></span>
<span data-ttu-id="6e129-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e129-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e129-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e129-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e129-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e129-132">INPUTS</span></span>

## <span data-ttu-id="6e129-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e129-133">OUTPUTS</span></span>

### <span data-ttu-id="6e129-134">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6e129-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="6e129-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e129-135">NOTES</span></span>

## <span data-ttu-id="6e129-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e129-136">RELATED LINKS</span></span>

[<span data-ttu-id="6e129-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6e129-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="6e129-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6e129-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="6e129-139">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6e129-139">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)

