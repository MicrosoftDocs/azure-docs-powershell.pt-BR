---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 7c6457e30140e10c5e6746c69a213f5ac4932cc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433060"
---
# <span data-ttu-id="df7c0-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="df7c0-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="df7c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="df7c0-103">Remove um certificado de revogação do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="df7c0-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df7c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df7c0-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df7c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df7c0-105">DESCRIPTION</span></span>
<span data-ttu-id="df7c0-106">O cmdlet **Remove-AzureRmVpnClientRevokedCertificate** remove um certificado de revogação de cliente de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="df7c0-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="df7c0-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="df7c0-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="df7c0-108">Se você remover um cliente de certificado de revogação de cliente, os computadores cliente poderão usar o certificado anteriormente proibido para fazer uma conexão de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="df7c0-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="df7c0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df7c0-109">EXAMPLES</span></span>

### <span data-ttu-id="df7c0-110">Exemplo 1: remover um certificado de revogação de cliente de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="df7c0-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="df7c0-111">Esse comando Remove um certificado de revogação de cliente de um gateway de rede virtual chamado ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="df7c0-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="df7c0-112">Para remover um certificado de revogação de cliente, você deve especificar o nome do certificado e a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="df7c0-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="df7c0-113">OS</span><span class="sxs-lookup"><span data-stu-id="df7c0-113">PARAMETERS</span></span>

### <span data-ttu-id="df7c0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7c0-114">-ResourceGroupName</span></span>
<span data-ttu-id="df7c0-115">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="df7c0-115">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="df7c0-116">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="df7c0-116">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="df7c0-117">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="df7c0-117">-Thumbprint</span></span>
<span data-ttu-id="df7c0-118">Especifica o identificador exclusivo do certificado que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="df7c0-118">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="df7c0-119">Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="df7c0-119">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="df7c0-120">O comando anterior retorna informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="df7c0-120">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="df7c0-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="df7c0-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="df7c0-122">Especifica o nome do gateway de rede virtual ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="df7c0-122">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="df7c0-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="df7c0-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="df7c0-124">Especifica o nome do certificado de cliente VPN que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="df7c0-124">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="df7c0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7c0-125">-DefaultProfile</span></span>
<span data-ttu-id="df7c0-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df7c0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df7c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7c0-127">CommonParameters</span></span>
<span data-ttu-id="df7c0-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7c0-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7c0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7c0-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df7c0-130">INPUTS</span></span>

## <span data-ttu-id="df7c0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df7c0-131">OUTPUTS</span></span>

## <span data-ttu-id="df7c0-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df7c0-132">NOTES</span></span>

## <span data-ttu-id="df7c0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df7c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="df7c0-134">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="df7c0-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="df7c0-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="df7c0-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="df7c0-136">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="df7c0-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

