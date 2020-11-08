---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118415"
---
# <span data-ttu-id="deae6-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="deae6-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="deae6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deae6-102">SYNOPSIS</span></span>
<span data-ttu-id="deae6-103">Obtém as chaves de API para uma conta.</span><span class="sxs-lookup"><span data-stu-id="deae6-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="deae6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deae6-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deae6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="deae6-105">DESCRIPTION</span></span>
<span data-ttu-id="deae6-106">O cmdlet **Get-AzCognitiveServicesAccountKey** Obtém as chaves de API para uma conta provisionada de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="deae6-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="deae6-107">Uma conta de serviços cognitivas tem duas chaves de API: key1 e Key2.</span><span class="sxs-lookup"><span data-stu-id="deae6-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="deae6-108">As chaves permitem a interação com o ponto de extremidade da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="deae6-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="deae6-109">Use New-AzCognitiveServicesAccountKey para gerar novamente uma chave.</span><span class="sxs-lookup"><span data-stu-id="deae6-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="deae6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="deae6-110">EXAMPLES</span></span>

### <span data-ttu-id="deae6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="deae6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="deae6-112">OS</span><span class="sxs-lookup"><span data-stu-id="deae6-112">PARAMETERS</span></span>

### <span data-ttu-id="deae6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deae6-113">-DefaultProfile</span></span>
<span data-ttu-id="deae6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="deae6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="deae6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="deae6-115">-Name</span></span>
<span data-ttu-id="deae6-116">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="deae6-116">Specifies the name of the account.</span></span>
<span data-ttu-id="deae6-117">Este cmdlet obtém as chaves para esta conta.</span><span class="sxs-lookup"><span data-stu-id="deae6-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="deae6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deae6-118">-ResourceGroupName</span></span>
<span data-ttu-id="deae6-119">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="deae6-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="deae6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deae6-120">CommonParameters</span></span>
<span data-ttu-id="deae6-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deae6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deae6-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deae6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deae6-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="deae6-123">INPUTS</span></span>

### <span data-ttu-id="deae6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="deae6-124">System.String</span></span>

## <span data-ttu-id="deae6-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="deae6-125">OUTPUTS</span></span>

### <span data-ttu-id="deae6-126">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="deae6-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="deae6-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="deae6-127">NOTES</span></span>

## <span data-ttu-id="deae6-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deae6-128">RELATED LINKS</span></span>

[<span data-ttu-id="deae6-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="deae6-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


