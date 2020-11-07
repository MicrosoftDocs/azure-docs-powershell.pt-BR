---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: f9dbdaf531f4ccc35543dc542dc0637b9795360e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775343"
---
# <span data-ttu-id="f0fca-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="f0fca-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="f0fca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0fca-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fca-103">Cria um novo cliente VPN-certificado de revogação.</span><span class="sxs-lookup"><span data-stu-id="f0fca-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="f0fca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0fca-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0fca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0fca-105">DESCRIPTION</span></span>
<span data-ttu-id="f0fca-106">O cmdlet **New-AzVpnClientRevokedCertificate** cria um novo cliente de rede virtual privada (VPN)-certificado de revogação para uso em um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="f0fca-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="f0fca-107">Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="f0fca-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="f0fca-108">Esse cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="f0fca-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="f0fca-109">Em vez disso, o certificado criado por **New-AzVpnClientRevokedCertificate** é usado em conjunto com o cmdlet New-AzVirtualNetworkGateway quando ele cria um novo gateway.</span><span class="sxs-lookup"><span data-stu-id="f0fca-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="f0fca-110">Por exemplo, suponha que você crie um novo certificado e o armazene em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="f0fca-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="f0fca-111">Em seguida, você pode usar esse objeto de certificado quando criar um novo gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="f0fca-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="f0fca-112">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="f0fca-112">For instance,</span></span>

`New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="f0fca-113">Para obter mais informações, consulte a documentação do cmdlet New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="f0fca-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="f0fca-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0fca-114">EXAMPLES</span></span>

### <span data-ttu-id="f0fca-115">Exemplo 1: criar um novo certificado revogado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="f0fca-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="f0fca-116">Esse comando cria um novo certificado revogado pelo cliente e armazena o objeto do certificado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="f0fca-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="f0fca-117">Essa variável pode ser usada pelo cmdlet **New-AzVirtualNetworkGateway** para adicionar o certificado a um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f0fca-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="f0fca-118">OS</span><span class="sxs-lookup"><span data-stu-id="f0fca-118">PARAMETERS</span></span>

### <span data-ttu-id="f0fca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fca-119">-DefaultProfile</span></span>
<span data-ttu-id="f0fca-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0fca-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0fca-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0fca-121">-Name</span></span>
<span data-ttu-id="f0fca-122">Especifica um nome exclusivo para o novo certificado de revogação de cliente.</span><span class="sxs-lookup"><span data-stu-id="f0fca-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="f0fca-123">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="f0fca-123">-Thumbprint</span></span>
<span data-ttu-id="f0fca-124">Especifica o identificador exclusivo do certificado que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="f0fca-124">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="f0fca-125">Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="f0fca-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="f0fca-126">O comando anterior retorna informações para todos os certificados do computador local encontrados no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="f0fca-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="f0fca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fca-127">CommonParameters</span></span>
<span data-ttu-id="f0fca-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0fca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fca-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0fca-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fca-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0fca-130">INPUTS</span></span>

###  
<span data-ttu-id="f0fca-131">Esse cmdlet não aceita entrada em pipeline.</span><span class="sxs-lookup"><span data-stu-id="f0fca-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="f0fca-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0fca-132">OUTPUTS</span></span>

###  
<span data-ttu-id="f0fca-133">Esse cmdlet cria novas instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="f0fca-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="f0fca-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0fca-134">NOTES</span></span>

## <span data-ttu-id="f0fca-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0fca-135">RELATED LINKS</span></span>

[<span data-ttu-id="f0fca-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="f0fca-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="f0fca-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="f0fca-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="f0fca-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="f0fca-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)

