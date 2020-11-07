---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: e2a2153ca9d75447603ce87c896720ece0f83a18
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786492"
---
# <span data-ttu-id="1c59e-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1c59e-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="1c59e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c59e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c59e-103">Adiciona um certificado de revogação do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="1c59e-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c59e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c59e-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c59e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c59e-105">DESCRIPTION</span></span>
<span data-ttu-id="1c59e-106">O cmdlet **Add-AzureRmVpnClientRevokedCertificate** atribui um certificado de revogação de cliente a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1c59e-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="1c59e-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="1c59e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="1c59e-108">Você precisa especificar o nome do certificado e a impressão digital do certificado para usar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c59e-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="1c59e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c59e-109">EXAMPLES</span></span>

### <span data-ttu-id="1c59e-110">Exemplo 1: adicionar um novo certificado de revogação de cliente a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="1c59e-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="1c59e-111">Esse comando adiciona um novo certificado de revogação de cliente ao gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="1c59e-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="1c59e-112">Para adicionar o certificado, você deve especificar o nome do certificado e a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="1c59e-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="1c59e-113">OS</span><span class="sxs-lookup"><span data-stu-id="1c59e-113">PARAMETERS</span></span>

### <span data-ttu-id="1c59e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c59e-114">-DefaultProfile</span></span>
<span data-ttu-id="1c59e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c59e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c59e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c59e-116">-ResourceGroupName</span></span>
<span data-ttu-id="1c59e-117">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="1c59e-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="1c59e-118">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c59e-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="1c59e-119">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="1c59e-119">-Thumbprint</span></span>
<span data-ttu-id="1c59e-120">Especifica o identificador exclusivo do certificado que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="1c59e-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="1c59e-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1c59e-121">For example:</span></span>

<span data-ttu-id="1c59e-122">-Impressão digital "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="1c59e-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="1c59e-123">Você pode obter informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="1c59e-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="1c59e-124">O comando anterior obtém informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="1c59e-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="1c59e-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1c59e-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1c59e-126">Especifica o nome do gateway de rede virtual onde o certificado deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="1c59e-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="1c59e-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="1c59e-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="1c59e-128">Especifica o nome do certificado de cliente VPN a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="1c59e-128">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="1c59e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c59e-129">CommonParameters</span></span>
<span data-ttu-id="1c59e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c59e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c59e-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c59e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c59e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c59e-132">INPUTS</span></span>

## <span data-ttu-id="1c59e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c59e-133">OUTPUTS</span></span>

### <span data-ttu-id="1c59e-134">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1c59e-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="1c59e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c59e-135">NOTES</span></span>

## <span data-ttu-id="1c59e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c59e-136">RELATED LINKS</span></span>

[<span data-ttu-id="1c59e-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1c59e-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="1c59e-138">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1c59e-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="1c59e-139">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1c59e-139">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


