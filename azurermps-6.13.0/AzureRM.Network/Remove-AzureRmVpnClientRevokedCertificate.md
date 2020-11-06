---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: e9095c5f2e8f2a9820214f1144f10f8049f22027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428455"
---
# <span data-ttu-id="80b63-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="80b63-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="80b63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80b63-102">SYNOPSIS</span></span>
<span data-ttu-id="80b63-103">Remove um certificado de revogação do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="80b63-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80b63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80b63-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80b63-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80b63-105">DESCRIPTION</span></span>
<span data-ttu-id="80b63-106">O cmdlet **Remove-AzureRmVpnClientRevokedCertificate** remove um certificado de revogação de cliente de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="80b63-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="80b63-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="80b63-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="80b63-108">Se você remover um cliente de certificado de revogação de cliente, os computadores cliente poderão usar o certificado anteriormente proibido para fazer uma conexão de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="80b63-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="80b63-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80b63-109">EXAMPLES</span></span>

### <span data-ttu-id="80b63-110">Exemplo 1: remover um certificado de revogação de cliente de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="80b63-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="80b63-111">Esse comando Remove um certificado de revogação de cliente de um gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="80b63-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="80b63-112">Para remover um certificado de revogação de cliente, você deve especificar o nome do certificado e a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="80b63-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="80b63-113">OS</span><span class="sxs-lookup"><span data-stu-id="80b63-113">PARAMETERS</span></span>

### <span data-ttu-id="80b63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b63-114">-DefaultProfile</span></span>
<span data-ttu-id="80b63-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80b63-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b63-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b63-116">-ResourceGroupName</span></span>
<span data-ttu-id="80b63-117">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="80b63-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="80b63-118">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="80b63-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="80b63-119">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="80b63-119">-Thumbprint</span></span>
<span data-ttu-id="80b63-120">Especifica o identificador exclusivo do certificado que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="80b63-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="80b63-121">Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="80b63-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="80b63-122">O comando anterior retorna informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="80b63-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="80b63-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="80b63-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="80b63-124">Especifica o nome do gateway de rede virtual ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="80b63-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="80b63-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="80b63-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="80b63-126">Especifica o nome do certificado de cliente VPN que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="80b63-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="80b63-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b63-127">CommonParameters</span></span>
<span data-ttu-id="80b63-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b63-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b63-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b63-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b63-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80b63-130">INPUTS</span></span>

### <span data-ttu-id="80b63-131">System. String</span><span class="sxs-lookup"><span data-stu-id="80b63-131">System.String</span></span>

## <span data-ttu-id="80b63-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80b63-132">OUTPUTS</span></span>

### <span data-ttu-id="80b63-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80b63-133">System.Boolean</span></span>

## <span data-ttu-id="80b63-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80b63-134">NOTES</span></span>

## <span data-ttu-id="80b63-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80b63-135">RELATED LINKS</span></span>

[<span data-ttu-id="80b63-136">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="80b63-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="80b63-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="80b63-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="80b63-138">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="80b63-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

