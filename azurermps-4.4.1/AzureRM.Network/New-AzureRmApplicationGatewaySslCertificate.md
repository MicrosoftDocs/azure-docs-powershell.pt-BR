---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: ad318c776662ebaeab3192ca584aa2aad7f2e20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429970"
---
# <span data-ttu-id="67f61-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67f61-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="67f61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67f61-102">SYNOPSIS</span></span>
<span data-ttu-id="67f61-103">Cria um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="67f61-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67f61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67f61-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67f61-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67f61-105">DESCRIPTION</span></span>
<span data-ttu-id="67f61-106">O cmdlet **New-AzureRmApplicationGatewaySslCertificate** cria um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="67f61-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="67f61-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67f61-107">EXAMPLES</span></span>

### <span data-ttu-id="67f61-108">Exemplo 1: criar um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="67f61-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\>$Cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="67f61-109">Esse comando cria um certificado SSL chamado Cert01 para o gateway do aplicativo padrão e armazena o resultado na variável chamada $Cert.</span><span class="sxs-lookup"><span data-stu-id="67f61-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="67f61-110">OS</span><span class="sxs-lookup"><span data-stu-id="67f61-110">PARAMETERS</span></span>

### <span data-ttu-id="67f61-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="67f61-111">-CertificateFile</span></span>
<span data-ttu-id="67f61-112">Especifica o caminho do arquivo. pfx do certificado SSL criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67f61-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="67f61-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="67f61-113">-Name</span></span>
<span data-ttu-id="67f61-114">Especifica o nome do certificado SSL criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67f61-114">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="67f61-115">-Senha</span><span class="sxs-lookup"><span data-stu-id="67f61-115">-Password</span></span>
<span data-ttu-id="67f61-116">Especifica a senha do SSL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="67f61-116">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="67f61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f61-117">-DefaultProfile</span></span>
<span data-ttu-id="67f61-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67f61-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67f61-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f61-119">CommonParameters</span></span>
<span data-ttu-id="67f61-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f61-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f61-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f61-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f61-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67f61-122">INPUTS</span></span>

### <span data-ttu-id="67f61-123">System. String</span><span class="sxs-lookup"><span data-stu-id="67f61-123">System.String</span></span>

## <span data-ttu-id="67f61-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67f61-124">OUTPUTS</span></span>

### <span data-ttu-id="67f61-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67f61-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="67f61-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67f61-126">NOTES</span></span>

## <span data-ttu-id="67f61-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67f61-127">RELATED LINKS</span></span>

[<span data-ttu-id="67f61-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67f61-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="67f61-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67f61-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="67f61-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67f61-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="67f61-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67f61-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)

