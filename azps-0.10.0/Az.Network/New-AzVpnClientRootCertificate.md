---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: bd260deb8e43450b2feacb3c60f34ed6cc4003be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775348"
---
# <span data-ttu-id="a86b7-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86b7-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="a86b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a86b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a86b7-103">Cria um novo certificado raiz de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="a86b7-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="a86b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a86b7-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a86b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a86b7-105">DESCRIPTION</span></span>
<span data-ttu-id="a86b7-106">O cmdlet **New-AzVpnClientRootCertificate** cria um novo certificado raiz de VPN para ser usado em um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="a86b7-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="a86b7-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="a86b7-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="a86b7-108">Esse cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="a86b7-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="a86b7-109">Em vez disso, o certificado criado por **New-AzVpnClientRootCertificate** é usado em conjunto com o cmdlet New-AzVirtualNetworkGateway ao criar um novo gateway.</span><span class="sxs-lookup"><span data-stu-id="a86b7-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="a86b7-110">Por exemplo, suponha que você crie um novo certificado e o armazene em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="a86b7-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="a86b7-111">Em seguida, você pode usar esse objeto de certificado ao criar um novo gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="a86b7-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="a86b7-112">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="a86b7-112">For instance,</span></span>

`New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="a86b7-113">Para obter mais informações, consulte a documentação do cmdlet New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a86b7-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="a86b7-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a86b7-114">EXAMPLES</span></span>

### <span data-ttu-id="a86b7-115">Exemplo 1: criar um certificado raiz aclient</span><span class="sxs-lookup"><span data-stu-id="a86b7-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="a86b7-116">Este exemplo cria um certificado raiz do cliente e armazena o objeto do certificado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="a86b7-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="a86b7-117">Essa variável pode ser usada pelo cmdlet **New-AzVirtualNetworkGateway** para adicionar um certificado raiz a um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a86b7-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="a86b7-118">O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado raiz; esses dados de texto são armazenados em uma variável chamada $Text.</span><span class="sxs-lookup"><span data-stu-id="a86b7-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="a86b7-119">Em seguida, o segundo comando usa um loop for para extrair todo o texto, exceto a primeira linha e a última linha, armazenando o texto extraído em uma variável chamada $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="a86b7-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="a86b7-120">O terceiro comando usa o cmdlet **New-AzVpnClientRootCertificate** para criar o certificado, armazenando o objeto criado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="a86b7-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="a86b7-121">OS</span><span class="sxs-lookup"><span data-stu-id="a86b7-121">PARAMETERS</span></span>

### <span data-ttu-id="a86b7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86b7-122">-DefaultProfile</span></span>
<span data-ttu-id="a86b7-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a86b7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a86b7-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a86b7-124">-Name</span></span>
<span data-ttu-id="a86b7-125">Especifica um nome para o novo certificado raiz do cliente.</span><span class="sxs-lookup"><span data-stu-id="a86b7-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="a86b7-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="a86b7-126">-PublicCertData</span></span>
<span data-ttu-id="a86b7-127">Especifica uma representação de texto do certificado raiz a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="a86b7-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="a86b7-128">Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="a86b7-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="a86b7-129">Você deve ver uma saída semelhante a esta (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):</span><span class="sxs-lookup"><span data-stu-id="a86b7-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="a86b7-130">-----Iniciar certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w----------término do certificado</span><span class="sxs-lookup"><span data-stu-id="a86b7-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="a86b7-131">O PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar-----de certificado) e a última linha (----------de certificado final) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="a86b7-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="a86b7-132">Você pode recuperar o PublicCertData usando comandos do Windows PowerShell semelhantes a isto:</span><span class="sxs-lookup"><span data-stu-id="a86b7-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="a86b7-133">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. Length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="a86b7-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="a86b7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86b7-134">CommonParameters</span></span>
<span data-ttu-id="a86b7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86b7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86b7-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a86b7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86b7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a86b7-137">INPUTS</span></span>

###  
<span data-ttu-id="a86b7-138">Esse cmdlet não aceita entrada em pipeline.</span><span class="sxs-lookup"><span data-stu-id="a86b7-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="a86b7-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a86b7-139">OUTPUTS</span></span>

###  
<span data-ttu-id="a86b7-140">Esse cmdlet cria novas instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="a86b7-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="a86b7-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a86b7-141">NOTES</span></span>

## <span data-ttu-id="a86b7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a86b7-142">RELATED LINKS</span></span>

[<span data-ttu-id="a86b7-143">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86b7-143">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="a86b7-144">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86b7-144">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="a86b7-145">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86b7-145">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


