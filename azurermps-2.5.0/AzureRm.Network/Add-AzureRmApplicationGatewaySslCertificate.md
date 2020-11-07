---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 65c178cc8cf293cf6c20e6262733031e377f61fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785340"
---
# <span data-ttu-id="6b096-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b096-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6b096-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b096-102">SYNOPSIS</span></span>
<span data-ttu-id="6b096-103">Adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6b096-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b096-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b096-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b096-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b096-105">DESCRIPTION</span></span>
<span data-ttu-id="6b096-106">O cmdlet **Add-AzureRmApplicationGatewaySslCertificate** adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6b096-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="6b096-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b096-107">EXAMPLES</span></span>

### <span data-ttu-id="6b096-108">Exemplo 1: adicionar um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6b096-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="6b096-109">Esse comando obtém um gateway do aplicativo chamado ApplicationGateway01 e, em seguida, adiciona um certificado SSL chamado Cert01 a ele.</span><span class="sxs-lookup"><span data-stu-id="6b096-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="6b096-110">OS</span><span class="sxs-lookup"><span data-stu-id="6b096-110">PARAMETERS</span></span>

### <span data-ttu-id="6b096-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b096-111">-ApplicationGateway</span></span>
<span data-ttu-id="6b096-112">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="6b096-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b096-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6b096-113">-CertificateFile</span></span>
<span data-ttu-id="6b096-114">Especifica o arquivo. pfx de um certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="6b096-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6b096-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b096-115">-DefaultProfile</span></span>
<span data-ttu-id="6b096-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b096-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b096-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b096-117">-Name</span></span>
<span data-ttu-id="6b096-118">Especifica o nome do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="6b096-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6b096-119">-Senha</span><span class="sxs-lookup"><span data-stu-id="6b096-119">-Password</span></span>
<span data-ttu-id="6b096-120">Especifica a senha do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="6b096-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6b096-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b096-121">CommonParameters</span></span>
<span data-ttu-id="6b096-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b096-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b096-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b096-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b096-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b096-124">INPUTS</span></span>

### <span data-ttu-id="6b096-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6b096-125">System.String</span></span>

## <span data-ttu-id="6b096-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b096-126">OUTPUTS</span></span>

### <span data-ttu-id="6b096-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b096-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b096-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b096-128">NOTES</span></span>

## <span data-ttu-id="6b096-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b096-129">RELATED LINKS</span></span>

[<span data-ttu-id="6b096-130">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b096-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b096-131">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b096-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b096-132">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b096-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b096-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b096-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


