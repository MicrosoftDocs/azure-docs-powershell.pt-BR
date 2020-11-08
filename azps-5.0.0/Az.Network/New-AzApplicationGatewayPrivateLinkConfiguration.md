---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125611"
---
# <span data-ttu-id="0dc30-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc30-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="0dc30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dc30-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc30-103">Cria uma configuração de vínculo particular para um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="0dc30-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="0dc30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dc30-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc30-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dc30-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc30-106">O cmdlet **New-AzApplicationGatewayPrivateLinkConfiguration** cria uma configuração PrivateLink para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc30-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="0dc30-107">A configuração do link particular deve ser associada a uma configuração de IP de front-end para habilitar a funcionalidade do link particular.</span><span class="sxs-lookup"><span data-stu-id="0dc30-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="0dc30-108">Uma configuração de link privado pode atmost ser associada a apenas uma configuração de IP de front-end no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0dc30-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="0dc30-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dc30-109">EXAMPLES</span></span>

### <span data-ttu-id="0dc30-110">Exemplo 1: criar uma configuração de link particular com uma única configuração de IP</span><span class="sxs-lookup"><span data-stu-id="0dc30-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="0dc30-111">Esse comando cria uma configuração PrivateLink chamada ' privateLinkConfig01 ' e armazena o resultado na variável chamada $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0dc30-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="0dc30-112">Exemplo 2: criar uma configuração de link particular com várias configurações de IP</span><span class="sxs-lookup"><span data-stu-id="0dc30-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="0dc30-113">Esse comando cria uma configuração PrivateLink chamada ' privateLinkConfig01 ' com duas ipConfigurations e armazena o resultado na variável chamada $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0dc30-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="0dc30-114">OS</span><span class="sxs-lookup"><span data-stu-id="0dc30-114">PARAMETERS</span></span>

### <span data-ttu-id="0dc30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc30-115">-DefaultProfile</span></span>
<span data-ttu-id="0dc30-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc30-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dc30-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc30-117">-IpConfiguration</span></span>
<span data-ttu-id="0dc30-118">A lista de ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc30-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc30-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0dc30-119">-Name</span></span>
<span data-ttu-id="0dc30-120">O nome da configuração do privateLink</span><span class="sxs-lookup"><span data-stu-id="0dc30-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="0dc30-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0dc30-121">-Confirm</span></span>
<span data-ttu-id="0dc30-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dc30-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc30-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc30-123">-WhatIf</span></span>
<span data-ttu-id="0dc30-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0dc30-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dc30-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0dc30-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc30-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc30-126">CommonParameters</span></span>
<span data-ttu-id="0dc30-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc30-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc30-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0dc30-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc30-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dc30-129">INPUTS</span></span>

### <span data-ttu-id="0dc30-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="0dc30-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="0dc30-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dc30-131">OUTPUTS</span></span>

### <span data-ttu-id="0dc30-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc30-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="0dc30-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dc30-133">NOTES</span></span>

## <span data-ttu-id="0dc30-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0dc30-134">RELATED LINKS</span></span>

[<span data-ttu-id="0dc30-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc30-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0dc30-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc30-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0dc30-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc30-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0dc30-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc30-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
