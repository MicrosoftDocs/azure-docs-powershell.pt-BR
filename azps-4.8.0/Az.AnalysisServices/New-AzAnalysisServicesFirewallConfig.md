---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 056a6e006cc0b1b3fd703757dcc07cbb0a8be987
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113405"
---
# <span data-ttu-id="ecfd4-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="ecfd4-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="ecfd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecfd4-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfd4-103">Cria uma nova configuração de firewall do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ecfd4-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="ecfd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecfd4-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecfd4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecfd4-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfd4-106">O New-AzAnalysisServicesFirewallConfig cria um novo objeto de configuração de firewall</span><span class="sxs-lookup"><span data-stu-id="ecfd4-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="ecfd4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecfd4-107">EXAMPLES</span></span>

### <span data-ttu-id="ecfd4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ecfd4-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="ecfd4-109">Cria um objeto de configuração de firewall com duas regras ao habilitar também o acesso do serviço do Power BI.</span><span class="sxs-lookup"><span data-stu-id="ecfd4-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="ecfd4-110">OS</span><span class="sxs-lookup"><span data-stu-id="ecfd4-110">PARAMETERS</span></span>

### <span data-ttu-id="ecfd4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfd4-111">-DefaultProfile</span></span>
<span data-ttu-id="ecfd4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfd4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfd4-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="ecfd4-113">-EnablePowerBIService</span></span>
<span data-ttu-id="ecfd4-114">Um sinalizador para indicar se o firewall está permitindo acesso do Power BI</span><span class="sxs-lookup"><span data-stu-id="ecfd4-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="ecfd4-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="ecfd4-115">-FirewallRule</span></span>
<span data-ttu-id="ecfd4-116">Uma lista de regras de firewall</span><span class="sxs-lookup"><span data-stu-id="ecfd4-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfd4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfd4-117">CommonParameters</span></span>
<span data-ttu-id="ecfd4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfd4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfd4-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfd4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfd4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecfd4-120">INPUTS</span></span>

### <span data-ttu-id="ecfd4-121">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. cmdlets. AnalysisServices, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ecfd4-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ecfd4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecfd4-122">OUTPUTS</span></span>

### <span data-ttu-id="ecfd4-123">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="ecfd4-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="ecfd4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecfd4-124">NOTES</span></span>

## <span data-ttu-id="ecfd4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecfd4-125">RELATED LINKS</span></span>

[<span data-ttu-id="ecfd4-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ecfd4-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)