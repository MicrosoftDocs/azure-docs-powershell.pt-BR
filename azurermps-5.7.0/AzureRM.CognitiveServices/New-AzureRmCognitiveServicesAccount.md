---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602168"
---
# <span data-ttu-id="b4480-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4480-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="b4480-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4480-102">SYNOPSIS</span></span>
<span data-ttu-id="b4480-103">Cria uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="b4480-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4480-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4480-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4480-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4480-105">DESCRIPTION</span></span>
<span data-ttu-id="b4480-106">O cmdlet **New-AzureRmCognitiveServicesAccount** cria uma conta de serviços cognitivas com o tipo e a SKU especificados.</span><span class="sxs-lookup"><span data-stu-id="b4480-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="b4480-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4480-107">EXAMPLES</span></span>

### <span data-ttu-id="b4480-108">1:</span><span class="sxs-lookup"><span data-stu-id="b4480-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="b4480-109">OS</span><span class="sxs-lookup"><span data-stu-id="b4480-109">PARAMETERS</span></span>

### <span data-ttu-id="b4480-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4480-110">-DefaultProfile</span></span>
<span data-ttu-id="b4480-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b4480-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4480-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b4480-112">-Force</span></span>
<span data-ttu-id="b4480-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b4480-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-114">-Local</span><span class="sxs-lookup"><span data-stu-id="b4480-114">-Location</span></span>
<span data-ttu-id="b4480-115">Especifica o local no qual criar a conta.</span><span class="sxs-lookup"><span data-stu-id="b4480-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4480-116">-Name</span></span>
<span data-ttu-id="b4480-117">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="b4480-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4480-118">-ResourceGroupName</span></span>
<span data-ttu-id="b4480-119">Especifica o nome do grupo de recursos ao qual a conta será atribuída.</span><span class="sxs-lookup"><span data-stu-id="b4480-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="b4480-120">O grupo de recursos já deve existir.</span><span class="sxs-lookup"><span data-stu-id="b4480-120">The resource group must already exist.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b4480-121">-SkuName</span></span>
<span data-ttu-id="b4480-122">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="b4480-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="b4480-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b4480-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4480-124">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="b4480-124">F0 (free tier)</span></span>
- <span data-ttu-id="b4480-125">S0</span><span class="sxs-lookup"><span data-stu-id="b4480-125">S0</span></span>
- <span data-ttu-id="b4480-126">Eles</span><span class="sxs-lookup"><span data-stu-id="b4480-126">S1</span></span>
- <span data-ttu-id="b4480-127">S2</span><span class="sxs-lookup"><span data-stu-id="b4480-127">S2</span></span>
- <span data-ttu-id="b4480-128">S3</span><span class="sxs-lookup"><span data-stu-id="b4480-128">S3</span></span>
- <span data-ttu-id="b4480-129">S4</span><span class="sxs-lookup"><span data-stu-id="b4480-129">S4</span></span>

<span data-ttu-id="b4480-130">Para obter mais informações, consulte [APIs de serviço cognitiva](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="b4480-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="b4480-131">-Tag</span></span>
<span data-ttu-id="b4480-132">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="b4480-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-133">-Digite</span><span class="sxs-lookup"><span data-stu-id="b4480-133">-Type</span></span>
<span data-ttu-id="b4480-134">Especifica o tipo de conta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="b4480-134">Specifies the type of account to create.</span></span> <span data-ttu-id="b4480-135">Os valores aceitáveis atuais para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b4480-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4480-136">Bing. sugestão automática. v7</span><span class="sxs-lookup"><span data-stu-id="b4480-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="b4480-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="b4480-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="b4480-138">Bing. Search. v7</span><span class="sxs-lookup"><span data-stu-id="b4480-138">Bing.Search.v7</span></span>
- <span data-ttu-id="b4480-139">Bing. Speech</span><span class="sxs-lookup"><span data-stu-id="b4480-139">Bing.Speech</span></span>
- <span data-ttu-id="b4480-140">Bing. verificador ortográfico. v7</span><span class="sxs-lookup"><span data-stu-id="b4480-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="b4480-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="b4480-141">ComputerVision</span></span>
- <span data-ttu-id="b4480-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="b4480-142">ContentModerator</span></span>
- <span data-ttu-id="b4480-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="b4480-143">CustomSpeech</span></span>
- <span data-ttu-id="b4480-144">CustomVision. previsão</span><span class="sxs-lookup"><span data-stu-id="b4480-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="b4480-145">CustomVision. Training</span><span class="sxs-lookup"><span data-stu-id="b4480-145">CustomVision.Training</span></span>
- <span data-ttu-id="b4480-146">Emoção</span><span class="sxs-lookup"><span data-stu-id="b4480-146">Emotion</span></span>
- <span data-ttu-id="b4480-147">Triste</span><span class="sxs-lookup"><span data-stu-id="b4480-147">Face</span></span>
- <span data-ttu-id="b4480-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="b4480-148">LUIS</span></span>
- <span data-ttu-id="b4480-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="b4480-149">QnAMaker</span></span>
- <span data-ttu-id="b4480-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="b4480-150">SpeakerRecognition</span></span>
- <span data-ttu-id="b4480-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="b4480-151">SpeechTranslation</span></span>
- <span data-ttu-id="b4480-152">Textanalytics</span><span class="sxs-lookup"><span data-stu-id="b4480-152">TextAnalytics</span></span>
- <span data-ttu-id="b4480-153">Texttranslation</span><span class="sxs-lookup"><span data-stu-id="b4480-153">TextTranslation</span></span>
- <span data-ttu-id="b4480-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="b4480-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4480-155">-Confirm</span></span>
<span data-ttu-id="b4480-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4480-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4480-157">-WhatIf</span></span>
<span data-ttu-id="b4480-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4480-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4480-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4480-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4480-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4480-160">CommonParameters</span></span>
<span data-ttu-id="b4480-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4480-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4480-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4480-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4480-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4480-163">INPUTS</span></span>

### <span data-ttu-id="b4480-164">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b4480-164">None</span></span>
<span data-ttu-id="b4480-165">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b4480-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4480-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4480-166">OUTPUTS</span></span>

### <span data-ttu-id="b4480-167">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4480-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="b4480-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4480-168">NOTES</span></span>

## <span data-ttu-id="b4480-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4480-169">RELATED LINKS</span></span>

[<span data-ttu-id="b4480-170">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4480-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b4480-171">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4480-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b4480-172">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4480-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
