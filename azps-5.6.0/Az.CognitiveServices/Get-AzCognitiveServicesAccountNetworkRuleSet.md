---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 60a61af31b5a7986779b19b893d4c02d0039ae49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892541"
---
# <span data-ttu-id="afad6-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="afad6-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="afad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afad6-102">SYNOPSIS</span></span>
<span data-ttu-id="afad6-103">Obter a propriedade NetworkRule de uma conta dos Serviços Cognitivos</span><span class="sxs-lookup"><span data-stu-id="afad6-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="afad6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="afad6-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afad6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="afad6-105">DESCRIPTION</span></span>
<span data-ttu-id="afad6-106">O cmdlet **Get-AzCognitiveServicesAccountNetworkRuleSet** obtém a propriedade NetworkRule de uma conta dos Serviços Cognitivos</span><span class="sxs-lookup"><span data-stu-id="afad6-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="afad6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afad6-107">EXAMPLES</span></span>

### <span data-ttu-id="afad6-108">Exemplo 1: Obter a propriedade NetworkRule de uma conta especificada dos Serviços Cognitivos</span><span class="sxs-lookup"><span data-stu-id="afad6-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="afad6-109">Este comando obtém a propriedade NetworkRule de uma conta especificada dos Serviços Cognitivos</span><span class="sxs-lookup"><span data-stu-id="afad6-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="afad6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="afad6-110">PARAMETERS</span></span>

### <span data-ttu-id="afad6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afad6-111">-DefaultProfile</span></span>
<span data-ttu-id="afad6-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afad6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afad6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="afad6-113">-Name</span></span>
<span data-ttu-id="afad6-114">Nome da conta dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="afad6-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afad6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afad6-115">-ResourceGroupName</span></span>
<span data-ttu-id="afad6-116">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="afad6-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afad6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afad6-117">CommonParameters</span></span>
<span data-ttu-id="afad6-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afad6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afad6-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afad6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afad6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afad6-120">INPUTS</span></span>

### <span data-ttu-id="afad6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="afad6-121">System.String</span></span>

## <span data-ttu-id="afad6-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="afad6-122">OUTPUTS</span></span>

### <span data-ttu-id="afad6-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="afad6-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="afad6-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="afad6-124">NOTES</span></span>

## <span data-ttu-id="afad6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afad6-125">RELATED LINKS</span></span>
