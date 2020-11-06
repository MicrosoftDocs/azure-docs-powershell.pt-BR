---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441200"
---
# <span data-ttu-id="3377c-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3377c-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="3377c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3377c-102">SYNOPSIS</span></span>
<span data-ttu-id="3377c-103">Cria uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="3377c-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3377c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3377c-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3377c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3377c-105">DESCRIPTION</span></span>
<span data-ttu-id="3377c-106">O cmdlet **New-AzureRmCognitiveServicesAccount** cria uma conta de serviços cognitivas com o tipo e a SKU especificados.</span><span class="sxs-lookup"><span data-stu-id="3377c-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="3377c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3377c-107">EXAMPLES</span></span>

### <span data-ttu-id="3377c-108">1:</span><span class="sxs-lookup"><span data-stu-id="3377c-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="3377c-109">OS</span><span class="sxs-lookup"><span data-stu-id="3377c-109">PARAMETERS</span></span>

### <span data-ttu-id="3377c-110">-Force</span><span class="sxs-lookup"><span data-stu-id="3377c-110">-Force</span></span>
<span data-ttu-id="3377c-111">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3377c-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3377c-112">-Local</span><span class="sxs-lookup"><span data-stu-id="3377c-112">-Location</span></span>
<span data-ttu-id="3377c-113">Especifica o local no qual criar a conta.</span><span class="sxs-lookup"><span data-stu-id="3377c-113">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="3377c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3377c-114">-Name</span></span>
<span data-ttu-id="3377c-115">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="3377c-115">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="3377c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3377c-116">-ResourceGroupName</span></span>
<span data-ttu-id="3377c-117">Especifica o nome do grupo de recursos ao qual a conta será atribuída.</span><span class="sxs-lookup"><span data-stu-id="3377c-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="3377c-118">O grupo de recursos já deve existir.</span><span class="sxs-lookup"><span data-stu-id="3377c-118">The resource group must already exist.</span></span>

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

### <span data-ttu-id="3377c-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3377c-119">-SkuName</span></span>
<span data-ttu-id="3377c-120">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="3377c-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="3377c-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3377c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3377c-122">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="3377c-122">F0 (free tier)</span></span>
- <span data-ttu-id="3377c-123">S0</span><span class="sxs-lookup"><span data-stu-id="3377c-123">S0</span></span>
- <span data-ttu-id="3377c-124">Eles</span><span class="sxs-lookup"><span data-stu-id="3377c-124">S1</span></span>
- <span data-ttu-id="3377c-125">S2</span><span class="sxs-lookup"><span data-stu-id="3377c-125">S2</span></span>
- <span data-ttu-id="3377c-126">S3</span><span class="sxs-lookup"><span data-stu-id="3377c-126">S3</span></span>
- <span data-ttu-id="3377c-127">S4</span><span class="sxs-lookup"><span data-stu-id="3377c-127">S4</span></span>

<span data-ttu-id="3377c-128">Para obter mais informações, consulte [APIs de serviço cognitiva](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="3377c-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="3377c-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="3377c-129">-Tag</span></span>
<span data-ttu-id="3377c-130">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="3377c-130">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="3377c-131">-Digite</span><span class="sxs-lookup"><span data-stu-id="3377c-131">-Type</span></span>
<span data-ttu-id="3377c-132">Especifica o tipo de conta a ser criada. Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3377c-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3377c-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="3377c-133">ComputerVision</span></span>
- <span data-ttu-id="3377c-134">Emoção</span><span class="sxs-lookup"><span data-stu-id="3377c-134">Emotion</span></span>
- <span data-ttu-id="3377c-135">Triste</span><span class="sxs-lookup"><span data-stu-id="3377c-135">Face</span></span>
- <span data-ttu-id="3377c-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="3377c-136">LUIS</span></span>
- <span data-ttu-id="3377c-137">Feitas</span><span class="sxs-lookup"><span data-stu-id="3377c-137">Recommendations</span></span>
- <span data-ttu-id="3377c-138">Curso</span><span class="sxs-lookup"><span data-stu-id="3377c-138">Speech</span></span>
- <span data-ttu-id="3377c-139">Textanalytics</span><span class="sxs-lookup"><span data-stu-id="3377c-139">TextAnalytics</span></span>
- <span data-ttu-id="3377c-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="3377c-140">WebLM</span></span>

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

### <span data-ttu-id="3377c-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3377c-141">-Confirm</span></span>
<span data-ttu-id="3377c-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3377c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3377c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3377c-143">-WhatIf</span></span>
<span data-ttu-id="3377c-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3377c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3377c-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3377c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3377c-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3377c-146">-DefaultProfile</span></span>
<span data-ttu-id="3377c-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3377c-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3377c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3377c-148">CommonParameters</span></span>
<span data-ttu-id="3377c-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3377c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3377c-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3377c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3377c-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3377c-151">INPUTS</span></span>

## <span data-ttu-id="3377c-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3377c-152">OUTPUTS</span></span>

### <span data-ttu-id="3377c-153">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3377c-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="3377c-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3377c-154">NOTES</span></span>

## <span data-ttu-id="3377c-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3377c-155">RELATED LINKS</span></span>

[<span data-ttu-id="3377c-156">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3377c-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="3377c-157">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3377c-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="3377c-158">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3377c-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
