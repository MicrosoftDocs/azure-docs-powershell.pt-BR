---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3288573719edac1f04b40ed624820397b4beebcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943950"
---
# <span data-ttu-id="9c6b6-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c6b6-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="9c6b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c6b6-102">SYNOPSIS</span></span>
<span data-ttu-id="9c6b6-103">Remove um certificado raiz de cliente VPN existente.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="9c6b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c6b6-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c6b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c6b6-105">DESCRIPTION</span></span>
<span data-ttu-id="9c6b6-106">O cmdlet **Remove-AzVpnClientRootCertificate** remove o certificado raiz especificado de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="9c6b6-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="9c6b6-108">Se você remover um certificado raiz que usa o certificado para fins de autenticação, ele não poderá mais se conectar ao gateway.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="9c6b6-109">Ao usar **Remove-AzVpnClientRootCertificate** , você deve fornecer o nome do certificado e uma representação de texto dos dados do certificado.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-109">When you use **Remove-AzVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="9c6b6-110">Para obter mais informações sobre a representação de texto de um certificado, consulte a descrição do parâmetro *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="9c6b6-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="9c6b6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c6b6-111">EXAMPLES</span></span>

### <span data-ttu-id="9c6b6-112">Exemplo 1: remover um certificado raiz de cliente de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="9c6b6-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="9c6b6-113">Este exemplo remove um certificado raiz de cliente chamado ContosoRootCertificate do gateway de rede virtual ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="9c6b6-114">O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado; Essa representação de texto é armazenada em uma variável chamada $Text.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="9c6b6-115">Em seguida, o segundo comando usa um loop for para extrair todo o texto no $Text, exceto a primeira linha e a última linha.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="9c6b6-116">Esse texto extraído é armazenado em uma variável chamada $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="9c6b6-117">O terceiro comando usa as informações armazenadas na variável $CertificateText juntamente com o cmdlet **Remove-AzVpnClientRootCertificate** para remover o certificado do gateway.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="9c6b6-118">OS</span><span class="sxs-lookup"><span data-stu-id="9c6b6-118">PARAMETERS</span></span>

### <span data-ttu-id="9c6b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c6b6-119">-DefaultProfile</span></span>
<span data-ttu-id="9c6b6-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c6b6-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="9c6b6-121">-PublicCertData</span></span>
<span data-ttu-id="9c6b6-122">Especifica a representação de texto do certificado raiz a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="9c6b6-123">Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="9c6b6-124">Você deve ver uma saída semelhante à seguinte (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):-----iniciar o certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----fim do certificado-----o PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar certificado-----) e a última linha (----------de certificado final) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="9c6b6-125">Você pode recuperar o PublicCertData usando comandos do Windows PowerShell semelhantes a este: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. Length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="9c6b6-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="9c6b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c6b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c6b6-127">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="9c6b6-128">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="9c6b6-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9c6b6-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9c6b6-130">Especifica o nome do gateway de rede virtual do qual o certificado será removido.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="9c6b6-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="9c6b6-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="9c6b6-132">Especifica o nome do certificado raiz do cliente que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c6b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c6b6-133">CommonParameters</span></span>
<span data-ttu-id="9c6b6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c6b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c6b6-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c6b6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c6b6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c6b6-136">INPUTS</span></span>

### <span data-ttu-id="9c6b6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9c6b6-137">System.String</span></span>

## <span data-ttu-id="9c6b6-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c6b6-138">OUTPUTS</span></span>

### <span data-ttu-id="9c6b6-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c6b6-139">System.Boolean</span></span>

## <span data-ttu-id="9c6b6-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c6b6-140">NOTES</span></span>

## <span data-ttu-id="9c6b6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c6b6-141">RELATED LINKS</span></span>

[<span data-ttu-id="9c6b6-142">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c6b6-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="9c6b6-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c6b6-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="9c6b6-144">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c6b6-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


