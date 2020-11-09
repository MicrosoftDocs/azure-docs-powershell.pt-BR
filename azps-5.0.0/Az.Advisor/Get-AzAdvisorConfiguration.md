---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284364"
---
# <span data-ttu-id="63d85-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="63d85-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="63d85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63d85-102">SYNOPSIS</span></span>
<span data-ttu-id="63d85-103">Obter as configurações do Azure Advisor para a assinatura ou o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="63d85-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="63d85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63d85-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63d85-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63d85-105">DESCRIPTION</span></span>
<span data-ttu-id="63d85-106">As configurações associadas a uma assinatura têm dois tipos:</span><span class="sxs-lookup"><span data-stu-id="63d85-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="63d85-107">Configuração de nível de assinatura: pode haver apenas uma configuração desse tipo para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="63d85-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="63d85-108">LowCpuThreshold e exclude são a única propriedade desse tipo de configuração.</span><span class="sxs-lookup"><span data-stu-id="63d85-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="63d85-109">Configuração do nível do nível de subfonte: pode haver apenas uma configuração para cada um dos seus Resources em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="63d85-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="63d85-110">Exclude é a única propriedade desse tipo de configuração.</span><span class="sxs-lookup"><span data-stu-id="63d85-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="63d85-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63d85-111">EXAMPLES</span></span>

### <span data-ttu-id="63d85-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63d85-112">Example 1</span></span>
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
<span data-ttu-id="63d85-113">Recupera uma lista de configurações do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="63d85-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="63d85-114">OS</span><span class="sxs-lookup"><span data-stu-id="63d85-114">PARAMETERS</span></span>

### <span data-ttu-id="63d85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d85-115">-DefaultProfile</span></span>
<span data-ttu-id="63d85-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63d85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63d85-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d85-117">-ResourceGroupName</span></span>
<span data-ttu-id="63d85-118">Nome do grupo de recursos da configuração</span><span class="sxs-lookup"><span data-stu-id="63d85-118">Resource Group name of the configuration</span></span>

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

### <span data-ttu-id="63d85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d85-119">CommonParameters</span></span>
<span data-ttu-id="63d85-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="63d85-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63d85-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d85-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63d85-122">INPUTS</span></span>

### <span data-ttu-id="63d85-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="63d85-123">None</span></span>

## <span data-ttu-id="63d85-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63d85-124">OUTPUTS</span></span>

### <span data-ttu-id="63d85-125">Microsoft. Azure. Commands. Advisor. cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="63d85-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="63d85-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63d85-126">NOTES</span></span>

## <span data-ttu-id="63d85-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63d85-127">RELATED LINKS</span></span>
