---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771471"
---
# <span data-ttu-id="1f032-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1f032-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="1f032-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f032-102">SYNOPSIS</span></span>
<span data-ttu-id="1f032-103">Atualiza uma política de firewall do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1f032-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="1f032-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f032-104">SYNTAX</span></span>

### <span data-ttu-id="1f032-105">ByFactoryObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f032-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f032-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="1f032-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f032-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f032-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f032-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f032-108">DESCRIPTION</span></span>
<span data-ttu-id="1f032-109">O cmdlet **set-AzApplicationGatewayFirewallPolicy** atualiza uma política de firewall do Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1f032-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="1f032-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f032-110">EXAMPLES</span></span>

### <span data-ttu-id="1f032-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f032-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="1f032-112">Esse comando atualiza a política de firewall do gateway do aplicativo com configurações na variável $AppGwFirewallPolicy e armazena o gateway atualizado na variável $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="1f032-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="1f032-113">OS</span><span class="sxs-lookup"><span data-stu-id="1f032-113">PARAMETERS</span></span>

### <span data-ttu-id="1f032-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f032-114">-AsJob</span></span>
<span data-ttu-id="1f032-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1f032-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="1f032-116">-CustomRule</span></span>
<span data-ttu-id="1f032-117">A lista de CustomRules</span><span class="sxs-lookup"><span data-stu-id="1f032-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f032-118">-DefaultProfile</span></span>
<span data-ttu-id="1f032-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f032-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f032-120">-InputObject</span></span>
<span data-ttu-id="1f032-121">O applicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1f032-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f032-122">-Name</span></span>
<span data-ttu-id="1f032-123">O nome da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="1f032-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f032-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f032-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f032-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f032-126">-ResourceId</span></span>
<span data-ttu-id="1f032-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f032-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f032-128">CommonParameters</span></span>
<span data-ttu-id="1f032-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f032-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f032-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f032-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f032-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f032-131">INPUTS</span></span>

### <span data-ttu-id="1f032-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1f032-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1f032-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f032-133">OUTPUTS</span></span>

### <span data-ttu-id="1f032-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1f032-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1f032-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f032-135">NOTES</span></span>

## <span data-ttu-id="1f032-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f032-136">RELATED LINKS</span></span>
