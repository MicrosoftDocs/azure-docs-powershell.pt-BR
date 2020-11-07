---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 7e249dc32be5c89483d575adf2d0eba8e407d1f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943953"
---
# <span data-ttu-id="c225e-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c225e-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c225e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c225e-102">SYNOPSIS</span></span>
<span data-ttu-id="c225e-103">Remove um certificado de revogação do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="c225e-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="c225e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c225e-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c225e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c225e-105">DESCRIPTION</span></span>
<span data-ttu-id="c225e-106">O cmdlet **Remove-AzVpnClientRevokedCertificate** remove um certificado de revogação de cliente de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c225e-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="c225e-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="c225e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="c225e-108">Se você remover um cliente de certificado de revogação de cliente, os computadores cliente poderão usar o certificado anteriormente proibido para fazer uma conexão de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="c225e-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="c225e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c225e-109">EXAMPLES</span></span>

### <span data-ttu-id="c225e-110">Exemplo 1: remover um certificado de revogação de cliente de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c225e-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="c225e-111">Esse comando Remove um certificado de revogação de cliente de um gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="c225e-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="c225e-112">Para remover um certificado de revogação de cliente, você deve especificar o nome do certificado e a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="c225e-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="c225e-113">OS</span><span class="sxs-lookup"><span data-stu-id="c225e-113">PARAMETERS</span></span>

### <span data-ttu-id="c225e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c225e-114">-DefaultProfile</span></span>
<span data-ttu-id="c225e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c225e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c225e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c225e-116">-ResourceGroupName</span></span>
<span data-ttu-id="c225e-117">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c225e-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="c225e-118">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="c225e-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="c225e-119">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="c225e-119">-Thumbprint</span></span>
<span data-ttu-id="c225e-120">Especifica o identificador exclusivo do certificado que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="c225e-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="c225e-121">Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="c225e-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="c225e-122">O comando anterior retorna informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="c225e-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="c225e-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c225e-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c225e-124">Especifica o nome do gateway de rede virtual ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c225e-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="c225e-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="c225e-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="c225e-126">Especifica o nome do certificado de cliente VPN que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="c225e-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="c225e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c225e-127">CommonParameters</span></span>
<span data-ttu-id="c225e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c225e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c225e-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c225e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c225e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c225e-130">INPUTS</span></span>

### <span data-ttu-id="c225e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c225e-131">System.String</span></span>

## <span data-ttu-id="c225e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c225e-132">OUTPUTS</span></span>

### <span data-ttu-id="c225e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c225e-133">System.Boolean</span></span>

## <span data-ttu-id="c225e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c225e-134">NOTES</span></span>

## <span data-ttu-id="c225e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c225e-135">RELATED LINKS</span></span>

[<span data-ttu-id="c225e-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c225e-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="c225e-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c225e-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="c225e-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c225e-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


