---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263939"
---
# <span data-ttu-id="5af07-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5af07-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="5af07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5af07-102">SYNOPSIS</span></span>
<span data-ttu-id="5af07-103">Obter a propriedade NetworkRule de uma conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="5af07-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="5af07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5af07-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5af07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5af07-105">DESCRIPTION</span></span>
<span data-ttu-id="5af07-106">O cmdlet **Get-AzCognitiveServicesAccountNetworkRuleSet** Obtém a propriedade NetworkRule de uma conta de serviços cognitivas</span><span class="sxs-lookup"><span data-stu-id="5af07-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="5af07-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5af07-107">EXAMPLES</span></span>

### <span data-ttu-id="5af07-108">Exemplo 1: obter a propriedade NetworkRule de uma conta de serviços cognitivas especificada</span><span class="sxs-lookup"><span data-stu-id="5af07-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="5af07-109">Este comando obtém a propriedade NetworkRule de uma conta de serviços cognitivas especificada</span><span class="sxs-lookup"><span data-stu-id="5af07-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="5af07-110">OS</span><span class="sxs-lookup"><span data-stu-id="5af07-110">PARAMETERS</span></span>

### <span data-ttu-id="5af07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af07-111">-DefaultProfile</span></span>
<span data-ttu-id="5af07-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5af07-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af07-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5af07-113">-Name</span></span>
<span data-ttu-id="5af07-114">Nome da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="5af07-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="5af07-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af07-115">-ResourceGroupName</span></span>
<span data-ttu-id="5af07-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5af07-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="5af07-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af07-117">CommonParameters</span></span>
<span data-ttu-id="5af07-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af07-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af07-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5af07-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af07-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5af07-120">INPUTS</span></span>

### <span data-ttu-id="5af07-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5af07-121">System.String</span></span>

## <span data-ttu-id="5af07-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5af07-122">OUTPUTS</span></span>

### <span data-ttu-id="5af07-123">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5af07-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="5af07-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5af07-124">NOTES</span></span>

## <span data-ttu-id="5af07-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5af07-125">RELATED LINKS</span></span>
