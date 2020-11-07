---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775414"
---
# <span data-ttu-id="0437b-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0437b-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0437b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0437b-102">SYNOPSIS</span></span>
<span data-ttu-id="0437b-103">Cria um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0437b-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0437b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0437b-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0437b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0437b-105">DESCRIPTION</span></span>
<span data-ttu-id="0437b-106">O cmdlet **New-AzApplicationGatewaySslCertificate** cria um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0437b-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0437b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0437b-107">EXAMPLES</span></span>

### <span data-ttu-id="0437b-108">Exemplo 1: criar um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0437b-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="0437b-109">Esse comando cria um certificado SSL chamado Cert01 para o gateway do aplicativo padrão e armazena o resultado na variável chamada $Cert.</span><span class="sxs-lookup"><span data-stu-id="0437b-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="0437b-110">OS</span><span class="sxs-lookup"><span data-stu-id="0437b-110">PARAMETERS</span></span>

### <span data-ttu-id="0437b-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0437b-111">-CertificateFile</span></span>
<span data-ttu-id="0437b-112">Especifica o caminho do arquivo. pfx do certificado SSL criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0437b-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0437b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0437b-113">-DefaultProfile</span></span>
<span data-ttu-id="0437b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0437b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0437b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0437b-115">-Name</span></span>
<span data-ttu-id="0437b-116">Especifica o nome do certificado SSL criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0437b-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0437b-117">-Senha</span><span class="sxs-lookup"><span data-stu-id="0437b-117">-Password</span></span>
<span data-ttu-id="0437b-118">Especifica a senha do SSL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="0437b-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0437b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0437b-119">CommonParameters</span></span>
<span data-ttu-id="0437b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0437b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0437b-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0437b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0437b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0437b-122">INPUTS</span></span>

### <span data-ttu-id="0437b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0437b-123">System.String</span></span>

## <span data-ttu-id="0437b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0437b-124">OUTPUTS</span></span>

### <span data-ttu-id="0437b-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0437b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0437b-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0437b-126">NOTES</span></span>

## <span data-ttu-id="0437b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0437b-127">RELATED LINKS</span></span>

[<span data-ttu-id="0437b-128">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0437b-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0437b-129">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0437b-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0437b-130">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0437b-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0437b-131">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0437b-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


