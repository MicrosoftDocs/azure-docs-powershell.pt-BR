---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1af7ef3b60fa296a5fb8190675393a0726d0502b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428152"
---
# <span data-ttu-id="88549-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="88549-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="88549-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88549-102">SYNOPSIS</span></span>
<span data-ttu-id="88549-103">Define o estado da meta de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="88549-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88549-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88549-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88549-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88549-105">DESCRIPTION</span></span>
<span data-ttu-id="88549-106">O cmdlet **set-AzureRmApplicationGatewaySslCertificate** define o estado da meta de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="88549-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="88549-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88549-107">EXAMPLES</span></span>

### <span data-ttu-id="88549-108">Exemplo 1: definir o estado da meta de um certificado SSL</span><span class="sxs-lookup"><span data-stu-id="88549-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="88549-109">Esse comando define o estado da meta para um certificado SSL do gateway do aplicativo chamado ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="88549-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="88549-110">OS</span><span class="sxs-lookup"><span data-stu-id="88549-110">PARAMETERS</span></span>

### <span data-ttu-id="88549-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88549-111">-ApplicationGateway</span></span>
<span data-ttu-id="88549-112">Especifica o gateway do aplicativo com o qual o certificado SSL (Secure Socket Layer) está associado.</span><span class="sxs-lookup"><span data-stu-id="88549-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="88549-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="88549-113">-CertificateFile</span></span>
<span data-ttu-id="88549-114">Especifica o caminho do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="88549-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="88549-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88549-115">-DefaultProfile</span></span>
<span data-ttu-id="88549-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88549-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88549-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="88549-117">-Name</span></span>
<span data-ttu-id="88549-118">Especifica o nome do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="88549-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="88549-119">-Senha</span><span class="sxs-lookup"><span data-stu-id="88549-119">-Password</span></span>
<span data-ttu-id="88549-120">Especifica a senha do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="88549-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="88549-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88549-121">CommonParameters</span></span>
<span data-ttu-id="88549-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88549-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88549-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88549-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88549-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88549-124">INPUTS</span></span>

### <span data-ttu-id="88549-125">System. String</span><span class="sxs-lookup"><span data-stu-id="88549-125">System.String</span></span>

## <span data-ttu-id="88549-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88549-126">OUTPUTS</span></span>

### <span data-ttu-id="88549-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88549-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="88549-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88549-128">NOTES</span></span>

## <span data-ttu-id="88549-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88549-129">RELATED LINKS</span></span>

[<span data-ttu-id="88549-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="88549-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="88549-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="88549-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="88549-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="88549-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="88549-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="88549-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


