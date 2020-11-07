---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: b4ab525623dd6bcb5aee57aeecf70ae36bdac380
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775610"
---
# <span data-ttu-id="19b23-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="19b23-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="19b23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19b23-102">SYNOPSIS</span></span>
<span data-ttu-id="19b23-103">Adiciona um certificado raiz de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="19b23-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="19b23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19b23-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19b23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19b23-105">DESCRIPTION</span></span>
<span data-ttu-id="19b23-106">O cmdlet **Add-AzVpnClientRootCertificate** adiciona um certificado raiz a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19b23-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="19b23-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="19b23-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="19b23-108">Por design, todos os certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="19b23-108">By design, all certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="19b23-109">Esse cmdlet atribui um certificado existente como um certificado raiz de gateway.</span><span class="sxs-lookup"><span data-stu-id="19b23-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="19b23-110">Se você não tiver um certificado X. 509 disponível, poderá gerar um por meio da infraestrutura de chave pública ou usar um gerador de certificado, como makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="19b23-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>

<span data-ttu-id="19b23-111">Para adicionar um certificado raiz, você deve especificar o nome do certificado e fornecer uma representação somente texto do certificado (consulte *o parâmetro PublicCertData* para obter mais informações).</span><span class="sxs-lookup"><span data-stu-id="19b23-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="19b23-112">O Azure permite que você atribua mais de um certificado raiz a um gateway.</span><span class="sxs-lookup"><span data-stu-id="19b23-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="19b23-113">Geralmente, vários certificados raiz são implantados por organizações que incluem usuários de mais de uma empresa.</span><span class="sxs-lookup"><span data-stu-id="19b23-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="19b23-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19b23-114">EXAMPLES</span></span>

### <span data-ttu-id="19b23-115">Exemplo 1: adicionar um certificado raiz de cliente a um gateway virtual</span><span class="sxs-lookup"><span data-stu-id="19b23-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="19b23-116">Este exemplo adiciona um certificado raiz de cliente a um gateway virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="19b23-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="19b23-117">O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado raiz e armazena esses dados de texto na variável chamada $Text.</span><span class="sxs-lookup"><span data-stu-id="19b23-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>

<span data-ttu-id="19b23-118">Em seguida, o segundo comando usa um loop for para extrair todo o texto, exceto a primeira linha e a última linha.</span><span class="sxs-lookup"><span data-stu-id="19b23-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="19b23-119">O texto extraído é armazenado em uma variável chamada $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="19b23-119">The extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="19b23-120">Em seguida, o terceiro comando usa o texto armazenado no $CertificateText com o cmdlet **Add-AzVpnClientRootCertificate** para adicionar o certificado raiz ao gateway.</span><span class="sxs-lookup"><span data-stu-id="19b23-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="19b23-121">OS</span><span class="sxs-lookup"><span data-stu-id="19b23-121">PARAMETERS</span></span>

### <span data-ttu-id="19b23-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b23-122">-DefaultProfile</span></span>
<span data-ttu-id="19b23-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19b23-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19b23-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="19b23-124">-PublicCertData</span></span>
<span data-ttu-id="19b23-125">Especifica a representação de texto do certificado raiz a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="19b23-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="19b23-126">Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="19b23-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="19b23-127">Ao fazer isso, você verá uma saída semelhante à seguinte (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):</span><span class="sxs-lookup"><span data-stu-id="19b23-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="19b23-128">-----Iniciar certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w----------término do certificado</span><span class="sxs-lookup"><span data-stu-id="19b23-128">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="19b23-129">O PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar-----de certificado) e a última linha (----------de certificado final) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="19b23-129">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="19b23-130">Você pode recuperar esses dados usando comandos do Windows PowerShell semelhantes a isto: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="19b23-130">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="19b23-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b23-131">-ResourceGroupName</span></span>
<span data-ttu-id="19b23-132">Especifica o nome do grupo de recursos ao qual o certificado raiz está atribuído.</span><span class="sxs-lookup"><span data-stu-id="19b23-132">Specifies the name of the resource group that the root certificate is assigned to.</span></span>

<span data-ttu-id="19b23-133">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="19b23-133">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="19b23-134">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="19b23-134">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="19b23-135">Especifica o nome do gateway de rede virtual onde o certificado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="19b23-135">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="19b23-136">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="19b23-136">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="19b23-137">Especifica o nome do certificado raiz do cliente que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="19b23-137">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="19b23-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b23-138">CommonParameters</span></span>
<span data-ttu-id="19b23-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b23-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b23-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b23-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b23-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19b23-141">INPUTS</span></span>

## <span data-ttu-id="19b23-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19b23-142">OUTPUTS</span></span>

### <span data-ttu-id="19b23-143">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="19b23-143">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="19b23-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19b23-144">NOTES</span></span>

## <span data-ttu-id="19b23-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19b23-145">RELATED LINKS</span></span>

[<span data-ttu-id="19b23-146">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="19b23-146">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="19b23-147">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="19b23-147">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="19b23-148">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="19b23-148">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)

