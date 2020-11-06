---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41d217579175de3c1de6f36b6850dfd391ca04b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431078"
---
# <span data-ttu-id="de276-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="de276-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="de276-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de276-102">SYNOPSIS</span></span>
<span data-ttu-id="de276-103">Obtém uma conta.</span><span class="sxs-lookup"><span data-stu-id="de276-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de276-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de276-104">SYNTAX</span></span>

### <span data-ttu-id="de276-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="de276-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de276-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="de276-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de276-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de276-107">DESCRIPTION</span></span>
<span data-ttu-id="de276-108">O cmdlet **Get-AzureRmCognitiveServicesAccount** Obtém as contas provisionadas de serviços cognitivas no grupo de recursos especificado pelo parâmetro *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="de276-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="de276-109">Se você não especificar o parâmetro *ResoureGroupName* , esse cmdlet obterá todas as contas de serviços cognitivas para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="de276-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="de276-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de276-110">EXAMPLES</span></span>

## <span data-ttu-id="de276-111">OS</span><span class="sxs-lookup"><span data-stu-id="de276-111">PARAMETERS</span></span>

### <span data-ttu-id="de276-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de276-112">-DefaultProfile</span></span>
<span data-ttu-id="de276-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="de276-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de276-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="de276-114">-Name</span></span>
<span data-ttu-id="de276-115">Especifica o nome da conta de serviços cognitiva a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="de276-115">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de276-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de276-116">-ResourceGroupName</span></span>
<span data-ttu-id="de276-117">Especifica o nome do grupo de recursos ao qual a conta de serviços cognitiva está atribuída.</span><span class="sxs-lookup"><span data-stu-id="de276-117">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de276-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de276-118">CommonParameters</span></span>
<span data-ttu-id="de276-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de276-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de276-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de276-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de276-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de276-121">INPUTS</span></span>

### <span data-ttu-id="de276-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="de276-122">None</span></span>
<span data-ttu-id="de276-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="de276-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de276-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de276-124">OUTPUTS</span></span>

### <span data-ttu-id="de276-125">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="de276-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="de276-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de276-126">NOTES</span></span>

## <span data-ttu-id="de276-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de276-127">RELATED LINKS</span></span>

[<span data-ttu-id="de276-128">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="de276-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="de276-129">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="de276-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="de276-130">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="de276-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


