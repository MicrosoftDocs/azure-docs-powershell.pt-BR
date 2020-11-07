---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: a5f562fd05432abc502d648ca7fae614744e4f2c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786289"
---
# <span data-ttu-id="71cfd-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71cfd-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="71cfd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="71cfd-103">Cria um novo certificado raiz de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="71cfd-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71cfd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71cfd-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71cfd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71cfd-105">DESCRIPTION</span></span>
<span data-ttu-id="71cfd-106">O cmdlet **New-AzureRmVpnClientRootCertificate** cria um novo certificado raiz de VPN para ser usado em um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="71cfd-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="71cfd-107">Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="71cfd-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="71cfd-108">Esse cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="71cfd-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="71cfd-109">Em vez disso, o certificado criado por **New-AzureRmVpnClientRootCertificate** é usado em conjunto com o cmdlet New-AzureRmVirtualNetworkGateway ao criar um novo gateway.</span><span class="sxs-lookup"><span data-stu-id="71cfd-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="71cfd-110">Por exemplo, suponha que você crie um novo certificado e o armazene em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="71cfd-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="71cfd-111">Em seguida, você pode usar esse objeto de certificado ao criar um novo gateway virtual.</span><span class="sxs-lookup"><span data-stu-id="71cfd-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="71cfd-112">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="71cfd-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="71cfd-113">Para obter mais informações, consulte a documentação do cmdlet New-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="71cfd-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="71cfd-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71cfd-114">EXAMPLES</span></span>

### <span data-ttu-id="71cfd-115">Exemplo 1: criar um certificado raiz aclient</span><span class="sxs-lookup"><span data-stu-id="71cfd-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="71cfd-116">Este exemplo cria um certificado raiz do cliente e armazena o objeto do certificado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="71cfd-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="71cfd-117">Essa variável pode ser usada pelo cmdlet **New-AzureRmVirtualNetworkGateway** para adicionar um certificado raiz a um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="71cfd-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="71cfd-118">O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado raiz; esses dados de texto são armazenados em uma variável chamada $Text.</span><span class="sxs-lookup"><span data-stu-id="71cfd-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="71cfd-119">Em seguida, o segundo comando usa um loop for para extrair todo o texto, exceto a primeira linha e a última linha, armazenando o texto extraído em uma variável chamada $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="71cfd-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="71cfd-120">O terceiro comando usa o cmdlet **New-AzureRmVpnClientRootCertificate** para criar o certificado, armazenando o objeto criado em uma variável chamada $Certificate.</span><span class="sxs-lookup"><span data-stu-id="71cfd-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="71cfd-121">OS</span><span class="sxs-lookup"><span data-stu-id="71cfd-121">PARAMETERS</span></span>

### <span data-ttu-id="71cfd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cfd-122">-DefaultProfile</span></span>
<span data-ttu-id="71cfd-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71cfd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71cfd-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="71cfd-124">-Name</span></span>
<span data-ttu-id="71cfd-125">Especifica um nome para o novo certificado raiz do cliente.</span><span class="sxs-lookup"><span data-stu-id="71cfd-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="71cfd-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="71cfd-126">-PublicCertData</span></span>
<span data-ttu-id="71cfd-127">Especifica uma representação de texto do certificado raiz a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="71cfd-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="71cfd-128">Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="71cfd-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="71cfd-129">Você deve ver uma saída semelhante a esta (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):</span><span class="sxs-lookup"><span data-stu-id="71cfd-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="71cfd-130">-----Iniciar certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w----------término do certificado</span><span class="sxs-lookup"><span data-stu-id="71cfd-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="71cfd-131">O PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar-----de certificado) e a última linha (----------de certificado final) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="71cfd-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="71cfd-132">Você pode recuperar o PublicCertData usando comandos do Windows PowerShell semelhantes a isto:</span><span class="sxs-lookup"><span data-stu-id="71cfd-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="71cfd-133">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. Length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="71cfd-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="71cfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cfd-134">CommonParameters</span></span>
<span data-ttu-id="71cfd-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71cfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cfd-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71cfd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cfd-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71cfd-137">INPUTS</span></span>

###  
<span data-ttu-id="71cfd-138">Esse cmdlet não aceita entrada em pipeline.</span><span class="sxs-lookup"><span data-stu-id="71cfd-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="71cfd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71cfd-139">OUTPUTS</span></span>

###  
<span data-ttu-id="71cfd-140">Esse cmdlet cria novas instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="71cfd-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="71cfd-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71cfd-141">NOTES</span></span>

## <span data-ttu-id="71cfd-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71cfd-142">RELATED LINKS</span></span>

[<span data-ttu-id="71cfd-143">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71cfd-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="71cfd-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71cfd-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="71cfd-145">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71cfd-145">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


