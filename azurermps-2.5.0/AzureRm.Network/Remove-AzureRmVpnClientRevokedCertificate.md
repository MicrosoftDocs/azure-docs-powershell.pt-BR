---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: ce4d2c61feb20c750d908b6f235d89dafa713e62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786409"
---
# <span data-ttu-id="fad6c-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fad6c-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="fad6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fad6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fad6c-103">Remove um certificado de revogação do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="fad6c-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fad6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fad6c-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fad6c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fad6c-105">DESCRIPTION</span></span>
<span data-ttu-id="fad6c-106">O cmdlet **Remove-AzureRmVpnClientRevokedCertificate** remove um certificado de revogação de cliente de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fad6c-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="fad6c-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="fad6c-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="fad6c-108">Se você remover um cliente de certificado de revogação de cliente, os computadores cliente poderão usar o certificado anteriormente proibido para fazer uma conexão de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="fad6c-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="fad6c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fad6c-109">EXAMPLES</span></span>

### <span data-ttu-id="fad6c-110">Exemplo 1: remover um certificado de revogação de cliente de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="fad6c-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="fad6c-111">Esse comando Remove um certificado de revogação de cliente de um gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="fad6c-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="fad6c-112">Para remover um certificado de revogação de cliente, você deve especificar o nome do certificado e a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="fad6c-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="fad6c-113">OS</span><span class="sxs-lookup"><span data-stu-id="fad6c-113">PARAMETERS</span></span>

### <span data-ttu-id="fad6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad6c-114">-DefaultProfile</span></span>
<span data-ttu-id="fad6c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fad6c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fad6c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad6c-116">-ResourceGroupName</span></span>
<span data-ttu-id="fad6c-117">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fad6c-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="fad6c-118">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="fad6c-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="fad6c-119">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="fad6c-119">-Thumbprint</span></span>
<span data-ttu-id="fad6c-120">Especifica o identificador exclusivo do certificado que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="fad6c-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="fad6c-121">Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="fad6c-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="fad6c-122">O comando anterior retorna informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="fad6c-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="fad6c-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="fad6c-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="fad6c-124">Especifica o nome do gateway de rede virtual ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fad6c-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="fad6c-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="fad6c-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="fad6c-126">Especifica o nome do certificado de cliente VPN que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="fad6c-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="fad6c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad6c-127">CommonParameters</span></span>
<span data-ttu-id="fad6c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad6c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad6c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad6c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad6c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fad6c-130">INPUTS</span></span>

## <span data-ttu-id="fad6c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fad6c-131">OUTPUTS</span></span>

## <span data-ttu-id="fad6c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fad6c-132">NOTES</span></span>

## <span data-ttu-id="fad6c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fad6c-133">RELATED LINKS</span></span>

[<span data-ttu-id="fad6c-134">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fad6c-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="fad6c-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fad6c-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="fad6c-136">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fad6c-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


