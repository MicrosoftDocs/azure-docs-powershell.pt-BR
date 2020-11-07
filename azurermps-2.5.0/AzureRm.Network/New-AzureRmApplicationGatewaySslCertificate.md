---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: e22760c2838cf0b4fb0597dbd45532374b604b79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785322"
---
# <span data-ttu-id="9f40c-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f40c-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9f40c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f40c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f40c-103">Cria um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f40c-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f40c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f40c-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f40c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f40c-105">DESCRIPTION</span></span>
<span data-ttu-id="9f40c-106">O cmdlet **New-AzureRmApplicationGatewaySslCertificate** cria um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f40c-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="9f40c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f40c-107">EXAMPLES</span></span>

### <span data-ttu-id="9f40c-108">Exemplo 1: criar um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f40c-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9f40c-109">Esse comando cria um certificado SSL chamado Cert01 para o gateway do aplicativo padrão e armazena o resultado na variável chamada $Cert.</span><span class="sxs-lookup"><span data-stu-id="9f40c-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="9f40c-110">OS</span><span class="sxs-lookup"><span data-stu-id="9f40c-110">PARAMETERS</span></span>

### <span data-ttu-id="9f40c-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9f40c-111">-CertificateFile</span></span>
<span data-ttu-id="9f40c-112">Especifica o caminho do arquivo. pfx do certificado SSL criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f40c-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9f40c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f40c-113">-DefaultProfile</span></span>
<span data-ttu-id="9f40c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f40c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f40c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f40c-115">-Name</span></span>
<span data-ttu-id="9f40c-116">Especifica o nome do certificado SSL criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f40c-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9f40c-117">-Senha</span><span class="sxs-lookup"><span data-stu-id="9f40c-117">-Password</span></span>
<span data-ttu-id="9f40c-118">Especifica a senha do SSL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="9f40c-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9f40c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f40c-119">CommonParameters</span></span>
<span data-ttu-id="9f40c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f40c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f40c-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f40c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f40c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f40c-122">INPUTS</span></span>

### <span data-ttu-id="9f40c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9f40c-123">System.String</span></span>

## <span data-ttu-id="9f40c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f40c-124">OUTPUTS</span></span>

### <span data-ttu-id="9f40c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f40c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9f40c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f40c-126">NOTES</span></span>

## <span data-ttu-id="9f40c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f40c-127">RELATED LINKS</span></span>

[<span data-ttu-id="9f40c-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f40c-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9f40c-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f40c-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9f40c-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f40c-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9f40c-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f40c-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


