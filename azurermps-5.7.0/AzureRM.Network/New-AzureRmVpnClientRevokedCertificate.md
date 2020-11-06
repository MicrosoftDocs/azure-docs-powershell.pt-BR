---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e4b9c5e921ce9a1b46e92b40b6877beb51dc709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432940"
---
# <span data-ttu-id="6264c-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6264c-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="6264c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6264c-102">SYNOPSIS</span></span>
<span data-ttu-id="6264c-103">Cria um novo cliente VPN-certificado de revogação.</span><span class="sxs-lookup"><span data-stu-id="6264c-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6264c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6264c-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6264c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6264c-105">DESCRIPTION</span></span>
<span data-ttu-id="6264c-106">O cmdlet **New-AzureRmVpnClientRevokedCertificate** cria um novo cliente de rede virtual privada (VPN)-certificado de revogação para uso em um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="6264c-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="6264c-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="6264c-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="6264c-108">Esse cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="6264c-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="6264c-109">Em vez disso, o certificado criado por **New-AzureRmVpnClientRevokedCertificate** é usado em conjunto com o cmdlet New-AzureRmVirtualNetworkGateway quando ele cria um novo gateway.</span><span class="sxs-lookup"><span data-stu-id="6264c-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="6264c-110">Por exemplo, suponha que você crie um novo certificado e o armazene em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="6264c-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="6264c-111">Em seguida, você pode usar esse objeto de certificado quando criar um novo gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="6264c-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="6264c-112">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="6264c-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="6264c-113">Para obter mais informações, consulte a documentação do cmdlet New-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="6264c-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="6264c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6264c-114">EXAMPLES</span></span>

### <span data-ttu-id="6264c-115">Exemplo 1: criar um novo certificado revogado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="6264c-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="6264c-116">Esse comando cria um novo certificado revogado pelo cliente e armazena o objeto do certificado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="6264c-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="6264c-117">Essa variável pode ser usada pelo cmdlet **New-AzureRmVirtualNetworkGateway** para adicionar o certificado a um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6264c-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="6264c-118">OS</span><span class="sxs-lookup"><span data-stu-id="6264c-118">PARAMETERS</span></span>

### <span data-ttu-id="6264c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6264c-119">-DefaultProfile</span></span>
<span data-ttu-id="6264c-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6264c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6264c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6264c-121">-Name</span></span>
<span data-ttu-id="6264c-122">Especifica um nome exclusivo para o novo certificado de revogação de cliente.</span><span class="sxs-lookup"><span data-stu-id="6264c-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="6264c-123">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="6264c-123">-Thumbprint</span></span>
<span data-ttu-id="6264c-124">Especifica o identificador exclusivo do certificado que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="6264c-124">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="6264c-125">Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="6264c-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="6264c-126">O comando anterior retorna informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="6264c-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="6264c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6264c-127">CommonParameters</span></span>
<span data-ttu-id="6264c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6264c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6264c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6264c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6264c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6264c-130">INPUTS</span></span>

###  
<span data-ttu-id="6264c-131">Esse cmdlet não aceita entrada em pipeline.</span><span class="sxs-lookup"><span data-stu-id="6264c-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="6264c-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6264c-132">OUTPUTS</span></span>

###  
<span data-ttu-id="6264c-133">Esse cmdlet cria novas instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="6264c-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="6264c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6264c-134">NOTES</span></span>

## <span data-ttu-id="6264c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6264c-135">RELATED LINKS</span></span>

[<span data-ttu-id="6264c-136">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6264c-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="6264c-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6264c-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="6264c-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6264c-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)

