---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113440"
---
# <span data-ttu-id="b2320-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b2320-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b2320-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2320-102">SYNOPSIS</span></span>
<span data-ttu-id="b2320-103">Atualiza o perfil SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b2320-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="b2320-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2320-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2320-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2320-105">DESCRIPTION</span></span>
<span data-ttu-id="b2320-106">O cmdlet **Set-AzApplicationGatewaySslProfile** atualiza o perfil SSL de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2320-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="b2320-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b2320-107">EXAMPLES</span></span>

### <span data-ttu-id="b2320-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2320-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="b2320-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b2320-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="b2320-110">O segundo comando atualiza o perfil SSL do gateway do aplicativo na variável $AppGw para atualizar a configuração de auth do cliente para o novo valor armazenado no $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="b2320-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="b2320-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2320-111">PARAMETERS</span></span>

### <span data-ttu-id="b2320-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2320-112">-ApplicationGateway</span></span>
<span data-ttu-id="b2320-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2320-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b2320-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2320-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="b2320-115">Configurações de configuração de autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="b2320-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2320-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2320-116">-DefaultProfile</span></span>
<span data-ttu-id="b2320-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2320-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2320-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2320-118">-Name</span></span>
<span data-ttu-id="b2320-119">O nome do perfil SSL</span><span class="sxs-lookup"><span data-stu-id="b2320-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="b2320-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="b2320-120">-SslPolicy</span></span>
<span data-ttu-id="b2320-121">Política SSL</span><span class="sxs-lookup"><span data-stu-id="b2320-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2320-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="b2320-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="b2320-123">As cadeias de certificados de certificação de cliente confiáveis</span><span class="sxs-lookup"><span data-stu-id="b2320-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2320-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2320-124">CommonParameters</span></span>
<span data-ttu-id="b2320-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2320-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2320-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2320-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2320-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="b2320-127">INPUTS</span></span>

### <span data-ttu-id="b2320-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2320-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b2320-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="b2320-129">OUTPUTS</span></span>

### <span data-ttu-id="b2320-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2320-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b2320-131">Notas</span><span class="sxs-lookup"><span data-stu-id="b2320-131">NOTES</span></span>

## <span data-ttu-id="b2320-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2320-132">RELATED LINKS</span></span>

[<span data-ttu-id="b2320-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b2320-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="b2320-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b2320-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="b2320-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b2320-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="b2320-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b2320-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)