---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112432"
---
# <span data-ttu-id="50fdc-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="50fdc-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="50fdc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="50fdc-103">Obtém uma conta.</span><span class="sxs-lookup"><span data-stu-id="50fdc-103">Gets an account.</span></span>

## <span data-ttu-id="50fdc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50fdc-104">SYNTAX</span></span>

### <span data-ttu-id="50fdc-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="50fdc-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50fdc-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50fdc-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50fdc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50fdc-107">DESCRIPTION</span></span>
<span data-ttu-id="50fdc-108">O cmdlet **Get-AzCognitiveServicesAccount** Obtém as contas provisionadas de serviços cognitivas no grupo de recursos especificado pelo parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="50fdc-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="50fdc-109">Se você não especificar o parâmetro *ResourceGroupName* , esse cmdlet obterá todas as contas de serviços cognitivas para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="50fdc-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="50fdc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50fdc-110">EXAMPLES</span></span>

### <span data-ttu-id="50fdc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50fdc-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="50fdc-112">OS</span><span class="sxs-lookup"><span data-stu-id="50fdc-112">PARAMETERS</span></span>

### <span data-ttu-id="50fdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fdc-113">-DefaultProfile</span></span>
<span data-ttu-id="50fdc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="50fdc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50fdc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="50fdc-115">-Name</span></span>
<span data-ttu-id="50fdc-116">Especifica o nome da conta de serviços cognitiva a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="50fdc-116">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fdc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50fdc-117">-ResourceGroupName</span></span>
<span data-ttu-id="50fdc-118">Especifica o nome do grupo de recursos ao qual a conta de serviços cognitiva está atribuída.</span><span class="sxs-lookup"><span data-stu-id="50fdc-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fdc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fdc-119">CommonParameters</span></span>
<span data-ttu-id="50fdc-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50fdc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fdc-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50fdc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fdc-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50fdc-122">INPUTS</span></span>

### <span data-ttu-id="50fdc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="50fdc-123">System.String</span></span>

## <span data-ttu-id="50fdc-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50fdc-124">OUTPUTS</span></span>

### <span data-ttu-id="50fdc-125">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="50fdc-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="50fdc-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50fdc-126">NOTES</span></span>

## <span data-ttu-id="50fdc-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50fdc-127">RELATED LINKS</span></span>

[<span data-ttu-id="50fdc-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="50fdc-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="50fdc-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="50fdc-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="50fdc-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="50fdc-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


