---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429815"
---
# <span data-ttu-id="3aeae-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="3aeae-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="3aeae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3aeae-102">SYNOPSIS</span></span>
<span data-ttu-id="3aeae-103">Crie um objeto que representa as configurações de regra de rede.</span><span class="sxs-lookup"><span data-stu-id="3aeae-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="3aeae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3aeae-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aeae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3aeae-105">DESCRIPTION</span></span>
<span data-ttu-id="3aeae-106">Crie um objeto que representa as configurações de regra de rede que podem ser usadas ao criar um cofre.</span><span class="sxs-lookup"><span data-stu-id="3aeae-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="3aeae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3aeae-107">EXAMPLES</span></span>

### <span data-ttu-id="3aeae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3aeae-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="3aeae-109">Criando um novo cofre e especifica regras de rede para permitir o acesso ao endereço IP especificado da rede virtual identificada por $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="3aeae-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="3aeae-110">OS</span><span class="sxs-lookup"><span data-stu-id="3aeae-110">PARAMETERS</span></span>

### <span data-ttu-id="3aeae-111">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="3aeae-111">-Bypass</span></span>
<span data-ttu-id="3aeae-112">Especifica bypass da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="3aeae-112">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="3aeae-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="3aeae-113">-DefaultAction</span></span>
<span data-ttu-id="3aeae-114">Especifica a ação padrão da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="3aeae-114">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="3aeae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aeae-115">-DefaultProfile</span></span>
<span data-ttu-id="3aeae-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3aeae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aeae-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="3aeae-117">-IpAddressRange</span></span>
<span data-ttu-id="3aeae-118">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="3aeae-118">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="3aeae-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3aeae-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3aeae-120">Especifica o identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="3aeae-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="3aeae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aeae-121">CommonParameters</span></span>
<span data-ttu-id="3aeae-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aeae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aeae-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3aeae-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aeae-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3aeae-124">INPUTS</span></span>

### <span data-ttu-id="3aeae-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3aeae-125">None</span></span>

## <span data-ttu-id="3aeae-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3aeae-126">OUTPUTS</span></span>

### <span data-ttu-id="3aeae-127">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3aeae-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="3aeae-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3aeae-128">NOTES</span></span>

## <span data-ttu-id="3aeae-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3aeae-129">RELATED LINKS</span></span>
