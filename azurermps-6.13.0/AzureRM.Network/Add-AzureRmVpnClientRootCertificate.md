---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 5f642892413b027d3eee4dec3c0264587dbb02a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440362"
---
# <span data-ttu-id="340db-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="340db-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="340db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="340db-102">SYNOPSIS</span></span>
<span data-ttu-id="340db-103">Adiciona um certificado raiz de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="340db-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="340db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="340db-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="340db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="340db-105">DESCRIPTION</span></span>
<span data-ttu-id="340db-106">O cmdlet **Add-AzureRmVpnClientRootCertificate** adiciona um certificado raiz a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="340db-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="340db-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="340db-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="340db-108">Por design, todos os certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="340db-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="340db-109">Esse cmdlet atribui um certificado existente como um certificado raiz de gateway.</span><span class="sxs-lookup"><span data-stu-id="340db-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="340db-110">Se você não tiver um certificado X. 509 disponível, poderá gerar um por meio da infraestrutura de chave pública ou usar um gerador de certificado, como makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="340db-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="340db-111">Para adicionar um certificado raiz, você deve especificar o nome do certificado e fornecer uma representação somente texto do certificado (consulte *o parâmetro PublicCertData* para obter mais informações).</span><span class="sxs-lookup"><span data-stu-id="340db-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="340db-112">O Azure permite que você atribua mais de um certificado raiz a um gateway.</span><span class="sxs-lookup"><span data-stu-id="340db-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="340db-113">Geralmente, vários certificados raiz são implantados por organizações que incluem usuários de mais de uma empresa.</span><span class="sxs-lookup"><span data-stu-id="340db-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="340db-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="340db-114">EXAMPLES</span></span>

### <span data-ttu-id="340db-115">Exemplo 1: adicionar um certificado raiz de cliente a um gateway virtual</span><span class="sxs-lookup"><span data-stu-id="340db-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="340db-116">Este exemplo adiciona um certificado raiz de cliente a um gateway virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="340db-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="340db-117">O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado raiz e armazena esses dados de texto na variável chamada $Text.</span><span class="sxs-lookup"><span data-stu-id="340db-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="340db-118">Em seguida, o segundo comando usa um loop for para extrair todo o texto, exceto a primeira linha e a última linha.</span><span class="sxs-lookup"><span data-stu-id="340db-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="340db-119">O texto extraído é armazenado em uma variável chamada $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="340db-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="340db-120">Em seguida, o terceiro comando usa o texto armazenado no $CertificateText com o cmdlet **Add-AzureRmVpnClientRootCertificate** para adicionar o certificado raiz ao gateway.</span><span class="sxs-lookup"><span data-stu-id="340db-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="340db-121">OS</span><span class="sxs-lookup"><span data-stu-id="340db-121">PARAMETERS</span></span>

### <span data-ttu-id="340db-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340db-122">-DefaultProfile</span></span>
<span data-ttu-id="340db-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="340db-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="340db-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="340db-124">-PublicCertData</span></span>
<span data-ttu-id="340db-125">Especifica a representação de texto do certificado raiz a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="340db-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="340db-126">Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="340db-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="340db-127">Ao fazer isso, você verá uma saída semelhante à seguinte (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):-----iniciar certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----término do certificado-----o PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar certificado-----) e a última linha (----------de certificado final) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="340db-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="340db-128">Você pode recuperar esses dados usando comandos do Windows PowerShell semelhantes a isto: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="340db-128">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="340db-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340db-129">-ResourceGroupName</span></span>
<span data-ttu-id="340db-130">Especifica o nome do grupo de recursos ao qual o certificado raiz está atribuído.</span><span class="sxs-lookup"><span data-stu-id="340db-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="340db-131">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="340db-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="340db-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="340db-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="340db-133">Especifica o nome do gateway de rede virtual onde o certificado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="340db-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="340db-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="340db-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="340db-135">Especifica o nome do certificado raiz do cliente que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="340db-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="340db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340db-136">CommonParameters</span></span>
<span data-ttu-id="340db-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="340db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340db-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="340db-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340db-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="340db-139">INPUTS</span></span>

### <span data-ttu-id="340db-140">System. String</span><span class="sxs-lookup"><span data-stu-id="340db-140">System.String</span></span>

## <span data-ttu-id="340db-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="340db-141">OUTPUTS</span></span>

### <span data-ttu-id="340db-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="340db-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="340db-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="340db-143">NOTES</span></span>

## <span data-ttu-id="340db-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="340db-144">RELATED LINKS</span></span>

[<span data-ttu-id="340db-145">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="340db-145">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="340db-146">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="340db-146">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="340db-147">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="340db-147">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)

