---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 46da28f86cac8aed68724683aaa69fde8ea64a50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892543"
---
# <span data-ttu-id="ce4b1-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="ce4b1-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="ce4b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4b1-103">Obtém as chaves da API de uma conta.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="ce4b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ce4b1-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce4b1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ce4b1-105">DESCRIPTION</span></span>
<span data-ttu-id="ce4b1-106">O cmdlet **Get-AzCognitiveServicesAccountKey** obtém as chaves da API de uma conta provisionada dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="ce4b1-107">Uma conta dos Serviços Cognitivos tem duas chaves de API: Key1 e Key2.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="ce4b1-108">As teclas habilitam a interação com o ponto de extremidade da conta dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="ce4b1-109">Use New-AzCognitiveServicesAccountKey para regenerar uma chave.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="ce4b1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce4b1-110">EXAMPLES</span></span>

### <span data-ttu-id="ce4b1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce4b1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="ce4b1-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ce4b1-112">PARAMETERS</span></span>

### <span data-ttu-id="ce4b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4b1-113">-DefaultProfile</span></span>
<span data-ttu-id="ce4b1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ce4b1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce4b1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ce4b1-115">-Name</span></span>
<span data-ttu-id="ce4b1-116">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-116">Specifies the name of the account.</span></span>
<span data-ttu-id="ce4b1-117">Este cmdlet obtém as chaves dessa conta.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="ce4b1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce4b1-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce4b1-119">Especifica o nome do grupo de recursos ao que a conta é atribuída.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="ce4b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4b1-120">CommonParameters</span></span>
<span data-ttu-id="ce4b1-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce4b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4b1-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce4b1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4b1-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce4b1-123">INPUTS</span></span>

### <span data-ttu-id="ce4b1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ce4b1-124">System.String</span></span>

## <span data-ttu-id="ce4b1-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ce4b1-125">OUTPUTS</span></span>

### <span data-ttu-id="ce4b1-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ce4b1-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="ce4b1-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="ce4b1-127">NOTES</span></span>

## <span data-ttu-id="ce4b1-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce4b1-128">RELATED LINKS</span></span>

[<span data-ttu-id="ce4b1-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="ce4b1-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


