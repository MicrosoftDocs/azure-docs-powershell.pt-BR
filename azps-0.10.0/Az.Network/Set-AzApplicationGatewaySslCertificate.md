---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776555"
---
# <span data-ttu-id="e3f3a-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f3a-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e3f3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f3a-103">Define o estado da meta de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="e3f3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3f3a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3f3a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f3a-106">O cmdlet **set-AzApplicationGatewaySslCertificate** define o estado da meta de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="e3f3a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="e3f3a-108">Exemplo 1: definir o estado da meta de um certificado SSL</span><span class="sxs-lookup"><span data-stu-id="e3f3a-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e3f3a-109">Esse comando define o estado da meta para um certificado SSL do gateway do aplicativo chamado ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="e3f3a-110">OS</span><span class="sxs-lookup"><span data-stu-id="e3f3a-110">PARAMETERS</span></span>

### <span data-ttu-id="e3f3a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f3a-111">-ApplicationGateway</span></span>
<span data-ttu-id="e3f3a-112">Especifica o gateway do aplicativo com o qual o certificado SSL (Secure Socket Layer) está associado.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="e3f3a-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e3f3a-113">-CertificateFile</span></span>
<span data-ttu-id="e3f3a-114">Especifica o caminho do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="e3f3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f3a-115">-DefaultProfile</span></span>
<span data-ttu-id="e3f3a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f3a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3f3a-117">-Name</span></span>
<span data-ttu-id="e3f3a-118">Especifica o nome do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="e3f3a-119">-Senha</span><span class="sxs-lookup"><span data-stu-id="e3f3a-119">-Password</span></span>
<span data-ttu-id="e3f3a-120">Especifica a senha do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="e3f3a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f3a-121">CommonParameters</span></span>
<span data-ttu-id="e3f3a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f3a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f3a-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f3a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f3a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3f3a-124">INPUTS</span></span>

### <span data-ttu-id="e3f3a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e3f3a-125">System.String</span></span>

## <span data-ttu-id="e3f3a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3f3a-126">OUTPUTS</span></span>

### <span data-ttu-id="e3f3a-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f3a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3f3a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3f3a-128">NOTES</span></span>

## <span data-ttu-id="e3f3a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3f3a-129">RELATED LINKS</span></span>

[<span data-ttu-id="e3f3a-130">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f3a-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3f3a-131">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f3a-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3f3a-132">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f3a-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3f3a-133">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f3a-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


