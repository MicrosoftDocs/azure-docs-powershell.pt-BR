---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429585"
---
# <span data-ttu-id="a271b-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a271b-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="a271b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a271b-102">SYNOPSIS</span></span>
<span data-ttu-id="a271b-103">Cria uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="a271b-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a271b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a271b-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a271b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a271b-105">DESCRIPTION</span></span>
<span data-ttu-id="a271b-106">O cmdlet **New-AzureRmCognitiveServicesAccount** cria uma conta de serviços cognitivas com o tipo e a SKU especificados.</span><span class="sxs-lookup"><span data-stu-id="a271b-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="a271b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a271b-107">EXAMPLES</span></span>

### <span data-ttu-id="a271b-108">1:</span><span class="sxs-lookup"><span data-stu-id="a271b-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="a271b-109">OS</span><span class="sxs-lookup"><span data-stu-id="a271b-109">PARAMETERS</span></span>

### <span data-ttu-id="a271b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a271b-110">-DefaultProfile</span></span>
<span data-ttu-id="a271b-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a271b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a271b-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a271b-112">-Force</span></span>
<span data-ttu-id="a271b-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a271b-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a271b-114">-Local</span><span class="sxs-lookup"><span data-stu-id="a271b-114">-Location</span></span>
<span data-ttu-id="a271b-115">Especifica o local no qual criar a conta.</span><span class="sxs-lookup"><span data-stu-id="a271b-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a271b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a271b-116">-Name</span></span>
<span data-ttu-id="a271b-117">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="a271b-117">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="a271b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a271b-118">-ResourceGroupName</span></span>
<span data-ttu-id="a271b-119">Especifica o nome do grupo de recursos ao qual a conta será atribuída.</span><span class="sxs-lookup"><span data-stu-id="a271b-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="a271b-120">O grupo de recursos já deve existir.</span><span class="sxs-lookup"><span data-stu-id="a271b-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="a271b-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a271b-121">-SkuName</span></span>
<span data-ttu-id="a271b-122">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="a271b-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="a271b-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a271b-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a271b-124">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="a271b-124">F0 (free tier)</span></span>
- <span data-ttu-id="a271b-125">S0</span><span class="sxs-lookup"><span data-stu-id="a271b-125">S0</span></span>
- <span data-ttu-id="a271b-126">Eles</span><span class="sxs-lookup"><span data-stu-id="a271b-126">S1</span></span>
- <span data-ttu-id="a271b-127">S2</span><span class="sxs-lookup"><span data-stu-id="a271b-127">S2</span></span>
- <span data-ttu-id="a271b-128">S3</span><span class="sxs-lookup"><span data-stu-id="a271b-128">S3</span></span>
- <span data-ttu-id="a271b-129">S4 para obter mais informações, consulte [APIs de serviço cognitiva](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="a271b-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a271b-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="a271b-130">-Tag</span></span>
<span data-ttu-id="a271b-131">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="a271b-131">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a271b-132">-Digite</span><span class="sxs-lookup"><span data-stu-id="a271b-132">-Type</span></span>
<span data-ttu-id="a271b-133">Especifica o tipo de conta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="a271b-133">Specifies the type of account to create.</span></span> <span data-ttu-id="a271b-134">Use o `Get-AzureRmCognitiveServicesAccountType` cmdlet para obter os valores aceitáveis atuais.</span><span class="sxs-lookup"><span data-stu-id="a271b-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a271b-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a271b-135">-Confirm</span></span>
<span data-ttu-id="a271b-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a271b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a271b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a271b-137">-WhatIf</span></span>
<span data-ttu-id="a271b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a271b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a271b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a271b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a271b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a271b-140">CommonParameters</span></span>
<span data-ttu-id="a271b-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a271b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a271b-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a271b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a271b-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a271b-143">INPUTS</span></span>

### <span data-ttu-id="a271b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a271b-144">System.String</span></span>

## <span data-ttu-id="a271b-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a271b-145">OUTPUTS</span></span>

### <span data-ttu-id="a271b-146">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a271b-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="a271b-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a271b-147">NOTES</span></span>

## <span data-ttu-id="a271b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a271b-148">RELATED LINKS</span></span>

[<span data-ttu-id="a271b-149">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a271b-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a271b-150">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a271b-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a271b-151">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a271b-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
