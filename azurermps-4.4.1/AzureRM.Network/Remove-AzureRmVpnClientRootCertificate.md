---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 75d86c77b57511b5a3fefb9cc21a668a81446746
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602434"
---
# <span data-ttu-id="61803-101">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61803-101">Remove-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="61803-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61803-102">SYNOPSIS</span></span>
<span data-ttu-id="61803-103">Remove um certificado raiz de cliente VPN existente.</span><span class="sxs-lookup"><span data-stu-id="61803-103">Removes an existing VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61803-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61803-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61803-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61803-105">DESCRIPTION</span></span>
<span data-ttu-id="61803-106">O cmdlet **Remove-AzureRmVpnClientRootCertificate** remove o certificado raiz especificado de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="61803-106">The **Remove-AzureRmVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="61803-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="61803-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="61803-108">Se você remover um certificado raiz que usa o certificado para fins de autenticação, ele não poderá mais se conectar ao gateway.</span><span class="sxs-lookup"><span data-stu-id="61803-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>

<span data-ttu-id="61803-109">Ao usar **Remove-AzureRmVpnClientRootCertificate** , você deve fornecer o nome do certificado e uma representação de texto dos dados do certificado.</span><span class="sxs-lookup"><span data-stu-id="61803-109">When you use **Remove-AzureRmVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="61803-110">Para obter mais informações sobre a representação de texto de um certificado, consulte a descrição do parâmetro *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="61803-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="61803-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61803-111">EXAMPLES</span></span>

### <span data-ttu-id="61803-112">Exemplo 1: remover um certificado raiz de cliente de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="61803-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="61803-113">Este exemplo remove um certificado raiz de cliente chamado ContosoRootCertificate do gateway de rede virtual ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="61803-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>

<span data-ttu-id="61803-114">O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado; Essa representação de texto é armazenada em uma variável chamada $Text.</span><span class="sxs-lookup"><span data-stu-id="61803-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>

<span data-ttu-id="61803-115">Em seguida, o segundo comando usa um loop for para extrair todo o texto no $Text, exceto a primeira linha e a última linha.</span><span class="sxs-lookup"><span data-stu-id="61803-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="61803-116">Esse texto extraído é armazenado em uma variável chamada $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="61803-116">This extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="61803-117">O terceiro comando usa as informações armazenadas na variável $CertificateText juntamente com o cmdlet **Remove-AzureRmVpnClientRootCertificate** para remover o certificado do gateway.</span><span class="sxs-lookup"><span data-stu-id="61803-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzureRmVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="61803-118">OS</span><span class="sxs-lookup"><span data-stu-id="61803-118">PARAMETERS</span></span>

### <span data-ttu-id="61803-119">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="61803-119">-PublicCertData</span></span>
<span data-ttu-id="61803-120">Especifica a representação de texto do certificado raiz a ser removido.</span><span class="sxs-lookup"><span data-stu-id="61803-120">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="61803-121">Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="61803-121">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="61803-122">Você deve ver uma saída semelhante à seguinte (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):</span><span class="sxs-lookup"><span data-stu-id="61803-122">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="61803-123">-----Iniciar certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w----------término do certificado</span><span class="sxs-lookup"><span data-stu-id="61803-123">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="61803-124">O PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar-----de certificado) e a última linha (----------de certificado final) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="61803-124">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="61803-125">Você pode recuperar o PublicCertData usando comandos do Windows PowerShell semelhantes a isto:</span><span class="sxs-lookup"><span data-stu-id="61803-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="61803-126">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. Length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="61803-126">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="61803-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61803-127">-ResourceGroupName</span></span>
<span data-ttu-id="61803-128">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="61803-128">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="61803-129">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="61803-129">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="61803-130">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="61803-130">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="61803-131">Especifica o nome do gateway de rede virtual do qual o certificado será removido.</span><span class="sxs-lookup"><span data-stu-id="61803-131">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="61803-132">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="61803-132">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="61803-133">Especifica o nome do certificado raiz do cliente que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="61803-133">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61803-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61803-134">-DefaultProfile</span></span>
<span data-ttu-id="61803-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61803-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61803-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61803-136">CommonParameters</span></span>
<span data-ttu-id="61803-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61803-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61803-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61803-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61803-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61803-139">INPUTS</span></span>

## <span data-ttu-id="61803-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61803-140">OUTPUTS</span></span>

## <span data-ttu-id="61803-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61803-141">NOTES</span></span>

## <span data-ttu-id="61803-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61803-142">RELATED LINKS</span></span>

[<span data-ttu-id="61803-143">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61803-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="61803-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61803-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="61803-145">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61803-145">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)


