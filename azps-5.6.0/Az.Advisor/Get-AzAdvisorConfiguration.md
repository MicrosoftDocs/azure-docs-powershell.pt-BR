---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: dd5ca513c327a1ed5d045c3b0283a8b220f6a062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887264"
---
# <span data-ttu-id="d5ae4-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5ae4-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="d5ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ae4-103">Obter as configurações do Azure Advisor para a assinatura ou grupo de recursos determinado.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="d5ae4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d5ae4-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5ae4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d5ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ae4-106">As configurações associadas a uma assinatura têm dois tipos:</span><span class="sxs-lookup"><span data-stu-id="d5ae4-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="d5ae4-107">Configuração de nível de assinatura: só pode haver uma configuração desse tipo para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="d5ae4-108">LowCpuThreshold e Exclude são a única propriedade desse tipo de configuração.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="d5ae4-109">Configuração de nível resourceGroup: pode haver apenas uma configuração para cada ResourceGroup em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="d5ae4-110">Exclude é a única propriedade desse tipo de configuração.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="d5ae4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5ae4-111">EXAMPLES</span></span>

### <span data-ttu-id="d5ae4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5ae4-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="d5ae4-113">Recupera uma lista de configurações do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="d5ae4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d5ae4-114">PARAMETERS</span></span>

### <span data-ttu-id="d5ae4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ae4-115">-DefaultProfile</span></span>
<span data-ttu-id="d5ae4-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5ae4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ae4-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5ae4-118">Nome do Grupo de Recursos da configuração</span><span class="sxs-lookup"><span data-stu-id="d5ae4-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ae4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ae4-119">CommonParameters</span></span>
<span data-ttu-id="d5ae4-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d5ae4-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ae4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ae4-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5ae4-122">INPUTS</span></span>

### <span data-ttu-id="d5ae4-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d5ae4-123">None</span></span>

## <span data-ttu-id="d5ae4-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d5ae4-124">OUTPUTS</span></span>

### <span data-ttu-id="d5ae4-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="d5ae4-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="d5ae4-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="d5ae4-126">NOTES</span></span>

## <span data-ttu-id="d5ae4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5ae4-127">RELATED LINKS</span></span>
