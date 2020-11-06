---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: f9b9f48d671bd0cbae0b7f8a26eccb21f372c4ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431115"
---
# <span data-ttu-id="9f534-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9f534-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="9f534-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f534-102">SYNOPSIS</span></span>
<span data-ttu-id="9f534-103">Obtém as chaves de API para uma conta.</span><span class="sxs-lookup"><span data-stu-id="9f534-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f534-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f534-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f534-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f534-105">DESCRIPTION</span></span>
<span data-ttu-id="9f534-106">O cmdlet **Get-AzureRmCognitiveServicesAccountKey** Obtém as chaves de API para uma conta provisionada de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="9f534-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="9f534-107">Uma conta de serviços cognitivas tem duas chaves de API: key1 e Key2.</span><span class="sxs-lookup"><span data-stu-id="9f534-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="9f534-108">As chaves permitem a interação com o ponto de extremidade da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="9f534-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="9f534-109">Use New-AzureRmCognitiveServicesAccountKey para gerar novamente uma chave.</span><span class="sxs-lookup"><span data-stu-id="9f534-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="9f534-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f534-110">EXAMPLES</span></span>

## <span data-ttu-id="9f534-111">OS</span><span class="sxs-lookup"><span data-stu-id="9f534-111">PARAMETERS</span></span>

### <span data-ttu-id="9f534-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f534-112">-Name</span></span>
<span data-ttu-id="9f534-113">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="9f534-113">Specifies the name of the account.</span></span>
<span data-ttu-id="9f534-114">Este cmdlet obtém as chaves para esta conta.</span><span class="sxs-lookup"><span data-stu-id="9f534-114">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="9f534-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f534-115">-ResourceGroupName</span></span>
<span data-ttu-id="9f534-116">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="9f534-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="9f534-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f534-117">-DefaultProfile</span></span>
<span data-ttu-id="9f534-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f534-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f534-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f534-119">CommonParameters</span></span>
<span data-ttu-id="9f534-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f534-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f534-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f534-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f534-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f534-122">INPUTS</span></span>

## <span data-ttu-id="9f534-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f534-123">OUTPUTS</span></span>

### <span data-ttu-id="9f534-124">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9f534-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="9f534-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f534-125">NOTES</span></span>

## <span data-ttu-id="9f534-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f534-126">RELATED LINKS</span></span>

[<span data-ttu-id="9f534-127">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9f534-127">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


