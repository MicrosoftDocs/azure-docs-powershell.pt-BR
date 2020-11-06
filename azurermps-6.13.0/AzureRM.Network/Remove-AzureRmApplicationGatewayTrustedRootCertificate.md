---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: eecce510632e7eef3fc61cf53127777b93c81e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429446"
---
# <span data-ttu-id="205b3-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="205b3-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="205b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="205b3-102">SYNOPSIS</span></span>
<span data-ttu-id="205b3-103">Remove um certificado raiz confiável de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="205b3-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="205b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="205b3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayTrustedRootCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="205b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="205b3-105">DESCRIPTION</span></span>
<span data-ttu-id="205b3-106">O cmdlet **Remove-AzureRmApplicationGatewayTrustedRootCertificate** remove um certificado raiz confiável de um Application Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="205b3-106">The **Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="205b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="205b3-107">EXAMPLES</span></span>

### <span data-ttu-id="205b3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="205b3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="205b3-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $gw.</span><span class="sxs-lookup"><span data-stu-id="205b3-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="205b3-110">O segundo comando Remove o certificado raiz confiável chamado myRootCA do gateway do aplicativo armazenado em $gw.</span><span class="sxs-lookup"><span data-stu-id="205b3-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="205b3-111">O terceiro comando atualiza o Application Gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="205b3-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="205b3-112">OS</span><span class="sxs-lookup"><span data-stu-id="205b3-112">PARAMETERS</span></span>

### <span data-ttu-id="205b3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="205b3-113">-ApplicationGateway</span></span>
<span data-ttu-id="205b3-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="205b3-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205b3-115">-DefaultProfile</span></span>
<span data-ttu-id="205b3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="205b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205b3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="205b3-117">-Name</span></span>
<span data-ttu-id="205b3-118">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="205b3-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="205b3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="205b3-119">-Confirm</span></span>
<span data-ttu-id="205b3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="205b3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205b3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205b3-121">-WhatIf</span></span>
<span data-ttu-id="205b3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="205b3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205b3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="205b3-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205b3-124">CommonParameters</span></span>
<span data-ttu-id="205b3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205b3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205b3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205b3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="205b3-127">INPUTS</span></span>

### <span data-ttu-id="205b3-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="205b3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="205b3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="205b3-129">OUTPUTS</span></span>

### <span data-ttu-id="205b3-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="205b3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="205b3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="205b3-131">NOTES</span></span>

## <span data-ttu-id="205b3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="205b3-132">RELATED LINKS</span></span>
