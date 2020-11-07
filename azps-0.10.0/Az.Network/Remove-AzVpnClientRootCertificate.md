---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: e9a04e255c91df49471b5b7070f6b95c48d45ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776590"
---
# <span data-ttu-id="b9dae-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dae-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="b9dae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9dae-102">SYNOPSIS</span></span>
<span data-ttu-id="b9dae-103">Remove um certificado raiz de cliente VPN existente.</span><span class="sxs-lookup"><span data-stu-id="b9dae-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="b9dae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9dae-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9dae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9dae-105">DESCRIPTION</span></span>
<span data-ttu-id="b9dae-106">O cmdlet **Remove-AzVpnClientRootCertificate** remove o certificado raiz especificado de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b9dae-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="b9dae-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="b9dae-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="b9dae-108">Se você remover um certificado raiz que usa o certificado para fins de autenticação, ele não poderá mais se conectar ao gateway.</span><span class="sxs-lookup"><span data-stu-id="b9dae-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>

<span data-ttu-id="b9dae-109">Ao usar **Remove-AzVpnClientRootCertificate** , você deve fornecer o nome do certificado e uma representação de texto dos dados do certificado.</span><span class="sxs-lookup"><span data-stu-id="b9dae-109">When you use **Remove-AzVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="b9dae-110">Para obter mais informações sobre a representação de texto de um certificado, consulte a descrição do parâmetro *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="b9dae-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="b9dae-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9dae-111">EXAMPLES</span></span>

### <span data-ttu-id="b9dae-112">Exemplo 1: remover um certificado raiz de cliente de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b9dae-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="b9dae-113">Este exemplo remove um certificado raiz de cliente chamado ContosoRootCertificate do gateway de rede virtual ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="b9dae-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>

<span data-ttu-id="b9dae-114">O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado; Essa representação de texto é armazenada em uma variável chamada $Text.</span><span class="sxs-lookup"><span data-stu-id="b9dae-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>

<span data-ttu-id="b9dae-115">Em seguida, o segundo comando usa um loop for para extrair todo o texto no $Text, exceto a primeira linha e a última linha.</span><span class="sxs-lookup"><span data-stu-id="b9dae-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="b9dae-116">Esse texto extraído é armazenado em uma variável chamada $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="b9dae-116">This extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="b9dae-117">O terceiro comando usa as informações armazenadas na variável $CertificateText juntamente com o cmdlet **Remove-AzVpnClientRootCertificate** para remover o certificado do gateway.</span><span class="sxs-lookup"><span data-stu-id="b9dae-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="b9dae-118">OS</span><span class="sxs-lookup"><span data-stu-id="b9dae-118">PARAMETERS</span></span>

### <span data-ttu-id="b9dae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9dae-119">-DefaultProfile</span></span>
<span data-ttu-id="b9dae-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9dae-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9dae-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="b9dae-121">-PublicCertData</span></span>
<span data-ttu-id="b9dae-122">Especifica a representação de texto do certificado raiz a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b9dae-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="b9dae-123">Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="b9dae-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="b9dae-124">Você deve ver uma saída semelhante à seguinte (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):</span><span class="sxs-lookup"><span data-stu-id="b9dae-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="b9dae-125">-----Iniciar certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w----------término do certificado</span><span class="sxs-lookup"><span data-stu-id="b9dae-125">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="b9dae-126">O PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar-----de certificado) e a última linha (----------de certificado final) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="b9dae-126">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="b9dae-127">Você pode recuperar o PublicCertData usando comandos do Windows PowerShell semelhantes a isto:</span><span class="sxs-lookup"><span data-stu-id="b9dae-127">You can retrieve the PublicCertData using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="b9dae-128">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. Length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="b9dae-128">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="b9dae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9dae-129">-ResourceGroupName</span></span>
<span data-ttu-id="b9dae-130">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b9dae-130">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="b9dae-131">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9dae-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="b9dae-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b9dae-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b9dae-133">Especifica o nome do gateway de rede virtual do qual o certificado será removido.</span><span class="sxs-lookup"><span data-stu-id="b9dae-133">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="b9dae-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="b9dae-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="b9dae-135">Especifica o nome do certificado raiz do cliente que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b9dae-135">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9dae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9dae-136">CommonParameters</span></span>
<span data-ttu-id="b9dae-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9dae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9dae-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9dae-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9dae-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9dae-139">INPUTS</span></span>

## <span data-ttu-id="b9dae-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9dae-140">OUTPUTS</span></span>

## <span data-ttu-id="b9dae-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9dae-141">NOTES</span></span>

## <span data-ttu-id="b9dae-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9dae-142">RELATED LINKS</span></span>

[<span data-ttu-id="b9dae-143">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dae-143">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="b9dae-144">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dae-144">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="b9dae-145">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dae-145">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


