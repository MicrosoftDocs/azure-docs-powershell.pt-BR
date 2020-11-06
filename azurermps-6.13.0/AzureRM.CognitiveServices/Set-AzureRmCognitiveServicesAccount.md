---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602802"
---
# <span data-ttu-id="838b5-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="838b5-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="838b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="838b5-102">SYNOPSIS</span></span>
<span data-ttu-id="838b5-103">Modifica uma conta.</span><span class="sxs-lookup"><span data-stu-id="838b5-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="838b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="838b5-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="838b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="838b5-105">DESCRIPTION</span></span>
<span data-ttu-id="838b5-106">O cmdlet **set-AzureRmCognitiveServicesAccount** modifica a SKU ou marca da conta de serviços cognitivas especificada.</span><span class="sxs-lookup"><span data-stu-id="838b5-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="838b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="838b5-107">EXAMPLES</span></span>

### <span data-ttu-id="838b5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="838b5-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="838b5-109">OS</span><span class="sxs-lookup"><span data-stu-id="838b5-109">PARAMETERS</span></span>

### <span data-ttu-id="838b5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838b5-110">-DefaultProfile</span></span>
<span data-ttu-id="838b5-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="838b5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="838b5-112">-Force</span><span class="sxs-lookup"><span data-stu-id="838b5-112">-Force</span></span>
<span data-ttu-id="838b5-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="838b5-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="838b5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="838b5-114">-Name</span></span>
<span data-ttu-id="838b5-115">Especifica o nome da conta a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="838b5-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="838b5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="838b5-116">-ResourceGroupName</span></span>
<span data-ttu-id="838b5-117">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="838b5-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="838b5-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="838b5-118">-SkuName</span></span>
<span data-ttu-id="838b5-119">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="838b5-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="838b5-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="838b5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="838b5-121">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="838b5-121">F0 (free tier)</span></span>
- <span data-ttu-id="838b5-122">S0</span><span class="sxs-lookup"><span data-stu-id="838b5-122">S0</span></span>
- <span data-ttu-id="838b5-123">Eles</span><span class="sxs-lookup"><span data-stu-id="838b5-123">S1</span></span>
- <span data-ttu-id="838b5-124">S2</span><span class="sxs-lookup"><span data-stu-id="838b5-124">S2</span></span>
- <span data-ttu-id="838b5-125">S3</span><span class="sxs-lookup"><span data-stu-id="838b5-125">S3</span></span>
- <span data-ttu-id="838b5-126">S4</span><span class="sxs-lookup"><span data-stu-id="838b5-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838b5-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="838b5-127">-Tag</span></span>
<span data-ttu-id="838b5-128">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="838b5-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838b5-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="838b5-129">-Confirm</span></span>
<span data-ttu-id="838b5-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="838b5-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838b5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="838b5-131">-WhatIf</span></span>
<span data-ttu-id="838b5-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="838b5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="838b5-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="838b5-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838b5-134">CommonParameters</span></span>
<span data-ttu-id="838b5-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838b5-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838b5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838b5-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="838b5-137">INPUTS</span></span>

### <span data-ttu-id="838b5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="838b5-138">System.String</span></span>

### <span data-ttu-id="838b5-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="838b5-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="838b5-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="838b5-140">OUTPUTS</span></span>

### <span data-ttu-id="838b5-141">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="838b5-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="838b5-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="838b5-142">NOTES</span></span>

## <span data-ttu-id="838b5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="838b5-143">RELATED LINKS</span></span>

[<span data-ttu-id="838b5-144">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="838b5-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="838b5-145">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="838b5-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="838b5-146">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="838b5-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
