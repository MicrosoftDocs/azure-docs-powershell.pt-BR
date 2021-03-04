---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 5f63ee4d1c55211b13eb525a76547064e61cba48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891812"
---
# <span data-ttu-id="2bded-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="2bded-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="2bded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bded-102">SYNOPSIS</span></span>
<span data-ttu-id="2bded-103">Crie um objeto que represente as configurações de regra de rede.</span><span class="sxs-lookup"><span data-stu-id="2bded-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="2bded-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2bded-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bded-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2bded-105">DESCRIPTION</span></span>
<span data-ttu-id="2bded-106">Crie um objeto que represente as configurações de regra de rede que podem ser usadas ao criar um cofre.</span><span class="sxs-lookup"><span data-stu-id="2bded-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="2bded-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bded-107">EXAMPLES</span></span>

### <span data-ttu-id="2bded-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bded-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="2bded-109">Criando um novo cofre e especifica regras de rede para permitir o acesso ao endereço IP especificado da rede virtual identificada por $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="2bded-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="2bded-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2bded-110">PARAMETERS</span></span>

### <span data-ttu-id="2bded-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="2bded-111">-Bypass</span></span>
<span data-ttu-id="2bded-112">Especifica o bypass da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="2bded-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bded-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="2bded-113">-DefaultAction</span></span>
<span data-ttu-id="2bded-114">Especifica a ação padrão da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="2bded-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bded-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bded-115">-DefaultProfile</span></span>
<span data-ttu-id="2bded-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bded-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bded-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="2bded-117">-IpAddressRange</span></span>
<span data-ttu-id="2bded-118">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="2bded-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bded-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="2bded-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="2bded-120">Especifica o identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="2bded-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bded-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bded-121">CommonParameters</span></span>
<span data-ttu-id="2bded-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bded-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bded-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bded-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bded-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bded-124">INPUTS</span></span>

### <span data-ttu-id="2bded-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2bded-125">None</span></span>

## <span data-ttu-id="2bded-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2bded-126">OUTPUTS</span></span>

### <span data-ttu-id="2bded-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2bded-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="2bded-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="2bded-128">NOTES</span></span>

## <span data-ttu-id="2bded-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bded-129">RELATED LINKS</span></span>
