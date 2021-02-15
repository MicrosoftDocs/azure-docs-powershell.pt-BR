---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115102"
---
# <span data-ttu-id="31880-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31880-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="31880-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31880-102">SYNOPSIS</span></span>
<span data-ttu-id="31880-103">Cria um novo certificado de revogação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="31880-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="31880-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31880-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31880-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="31880-105">DESCRIPTION</span></span>
<span data-ttu-id="31880-106">O cmdlet **New-AzVpnClientRevokedCertificate** cria um novo certificado de revogação de cliente de rede virtual privada (VPN) para uso em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="31880-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="31880-107">Certificados de revogação de cliente impedem que computadores cliente usem o certificado especificado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="31880-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="31880-108">Este cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="31880-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="31880-109">Em vez disso, o certificado criado pelo **New-AzVpnClientRevokedCertificate** é usado em conjunto com o cmdlet New-AzVirtualNetworkGateway quando ele cria um novo gateway.</span><span class="sxs-lookup"><span data-stu-id="31880-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="31880-110">Por exemplo, suponha que você crie um novo certificado e armazene-o em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="31880-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="31880-111">Em seguida, você pode usar esse objeto de certificado ao criar um novo gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="31880-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="31880-112">Por exemplo, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="31880-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="31880-113">Para obter mais informações, consulte a documentação do cmdlet New-AzVirtualNetworkGateway dados.</span><span class="sxs-lookup"><span data-stu-id="31880-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="31880-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31880-114">EXAMPLES</span></span>

### <span data-ttu-id="31880-115">Exemplo 1: Criar um novo certificado revogado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="31880-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="31880-116">Esse comando cria um novo certificado revogado pelo cliente e armazena o objeto de certificado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="31880-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="31880-117">Essa variável pode ser usada pelo cmdlet **New-AzVirtualNetworkGateway** para adicionar o certificado a um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="31880-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="31880-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31880-118">PARAMETERS</span></span>

### <span data-ttu-id="31880-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31880-119">-DefaultProfile</span></span>
<span data-ttu-id="31880-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="31880-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31880-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="31880-121">-Name</span></span>
<span data-ttu-id="31880-122">Especifica um nome exclusivo para o novo certificado de revogação de cliente.</span><span class="sxs-lookup"><span data-stu-id="31880-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="31880-123">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="31880-123">-Thumbprint</span></span>
<span data-ttu-id="31880-124">Especifica o identificador exclusivo do certificado que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="31880-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="31880-125">Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="31880-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="31880-126">O comando anterior retorna informações para todos os certificados de Computador Local encontrados no armazenamento de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="31880-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="31880-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31880-127">CommonParameters</span></span>
<span data-ttu-id="31880-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31880-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31880-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31880-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31880-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="31880-130">INPUTS</span></span>

### <span data-ttu-id="31880-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="31880-131">None</span></span>

## <span data-ttu-id="31880-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="31880-132">OUTPUTS</span></span>

### <span data-ttu-id="31880-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31880-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="31880-134">Notas</span><span class="sxs-lookup"><span data-stu-id="31880-134">NOTES</span></span>

## <span data-ttu-id="31880-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31880-135">RELATED LINKS</span></span>

[<span data-ttu-id="31880-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31880-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="31880-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31880-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="31880-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31880-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


