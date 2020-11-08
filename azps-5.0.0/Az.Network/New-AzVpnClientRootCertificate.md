---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118247"
---
# <span data-ttu-id="95cd9-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="95cd9-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="95cd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="95cd9-103">Cria um novo certificado raiz de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="95cd9-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="95cd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95cd9-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95cd9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95cd9-105">DESCRIPTION</span></span>
<span data-ttu-id="95cd9-106">O cmdlet **New-AzVpnClientRootCertificate** cria um novo certificado raiz de VPN para ser usado em um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="95cd9-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="95cd9-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="95cd9-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="95cd9-108">Esse cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="95cd9-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="95cd9-109">Em vez disso, o certificado criado por **New-AzVpnClientRootCertificate** é usado em conjunto com o cmdlet New-AzVirtualNetworkGateway ao criar um novo gateway.</span><span class="sxs-lookup"><span data-stu-id="95cd9-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="95cd9-110">Por exemplo, suponha que você crie um novo certificado e o armazene em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="95cd9-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="95cd9-111">Em seguida, você pode usar esse objeto de certificado ao criar um novo gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="95cd9-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="95cd9-112">Por exemplo, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="95cd9-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="95cd9-113">Para obter mais informações, consulte a documentação do cmdlet New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="95cd9-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="95cd9-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95cd9-114">EXAMPLES</span></span>

### <span data-ttu-id="95cd9-115">Exemplo 1: criar um certificado raiz de cliente</span><span class="sxs-lookup"><span data-stu-id="95cd9-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="95cd9-116">Este exemplo cria um certificado raiz do cliente e armazena o objeto do certificado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="95cd9-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="95cd9-117">Essa variável pode ser usada pelo cmdlet **New-AzVirtualNetworkGateway** para adicionar um certificado raiz a um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="95cd9-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="95cd9-118">O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado raiz; esses dados de texto são armazenados em uma variável chamada $Text.</span><span class="sxs-lookup"><span data-stu-id="95cd9-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="95cd9-119">Em seguida, o segundo comando usa um loop for para extrair todo o texto, exceto a primeira linha e a última linha, armazenando o texto extraído em uma variável chamada $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="95cd9-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="95cd9-120">O terceiro comando usa o cmdlet **New-AzVpnClientRootCertificate** para criar o certificado, armazenando o objeto criado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="95cd9-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="95cd9-121">OS</span><span class="sxs-lookup"><span data-stu-id="95cd9-121">PARAMETERS</span></span>

### <span data-ttu-id="95cd9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95cd9-122">-DefaultProfile</span></span>
<span data-ttu-id="95cd9-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95cd9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95cd9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="95cd9-124">-Name</span></span>
<span data-ttu-id="95cd9-125">Especifica um nome para o novo certificado raiz do cliente.</span><span class="sxs-lookup"><span data-stu-id="95cd9-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="95cd9-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="95cd9-126">-PublicCertData</span></span>
<span data-ttu-id="95cd9-127">Especifica uma representação de texto do certificado raiz a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="95cd9-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="95cd9-128">Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="95cd9-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="95cd9-129">Você deve ver uma saída semelhante a esta (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):-----iniciar o certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----END CERTIFICATE-----o PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar-----de certificado) e a última linha (----------de certificado final) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="95cd9-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="95cd9-130">Você pode recuperar o PublicCertData usando comandos do Windows PowerShell semelhantes a este: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. Length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="95cd9-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="95cd9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95cd9-131">CommonParameters</span></span>
<span data-ttu-id="95cd9-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95cd9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95cd9-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95cd9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95cd9-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95cd9-134">INPUTS</span></span>

### <span data-ttu-id="95cd9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="95cd9-135">System.String</span></span>

## <span data-ttu-id="95cd9-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95cd9-136">OUTPUTS</span></span>

### <span data-ttu-id="95cd9-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="95cd9-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="95cd9-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95cd9-138">NOTES</span></span>

## <span data-ttu-id="95cd9-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95cd9-139">RELATED LINKS</span></span>

[<span data-ttu-id="95cd9-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="95cd9-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="95cd9-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="95cd9-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="95cd9-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="95cd9-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


