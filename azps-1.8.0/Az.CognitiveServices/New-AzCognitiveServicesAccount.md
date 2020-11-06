---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601389"
---
# <span data-ttu-id="25d80-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="25d80-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="25d80-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25d80-102">SYNOPSIS</span></span>
<span data-ttu-id="25d80-103">Cria uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="25d80-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="25d80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25d80-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d80-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25d80-105">DESCRIPTION</span></span>
<span data-ttu-id="25d80-106">O cmdlet **New-AzCognitiveServicesAccount** cria uma conta de serviços cognitivas com o tipo e a SKU especificados.</span><span class="sxs-lookup"><span data-stu-id="25d80-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="25d80-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25d80-107">EXAMPLES</span></span>

### <span data-ttu-id="25d80-108">1:</span><span class="sxs-lookup"><span data-stu-id="25d80-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="25d80-109">OS</span><span class="sxs-lookup"><span data-stu-id="25d80-109">PARAMETERS</span></span>

### <span data-ttu-id="25d80-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="25d80-110">-CustomSubdomainName</span></span>
<span data-ttu-id="25d80-111">Nome de subdomínio da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="25d80-111">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d80-112">-DefaultProfile</span></span>
<span data-ttu-id="25d80-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="25d80-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25d80-114">-Force</span><span class="sxs-lookup"><span data-stu-id="25d80-114">-Force</span></span>
<span data-ttu-id="25d80-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="25d80-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25d80-116">-Local</span><span class="sxs-lookup"><span data-stu-id="25d80-116">-Location</span></span>
<span data-ttu-id="25d80-117">Especifica o local no qual criar a conta.</span><span class="sxs-lookup"><span data-stu-id="25d80-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="25d80-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="25d80-118">-Name</span></span>
<span data-ttu-id="25d80-119">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="25d80-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="25d80-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d80-120">-ResourceGroupName</span></span>
<span data-ttu-id="25d80-121">Especifica o nome do grupo de recursos ao qual a conta será atribuída.</span><span class="sxs-lookup"><span data-stu-id="25d80-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="25d80-122">O grupo de recursos já deve existir.</span><span class="sxs-lookup"><span data-stu-id="25d80-122">The resource group must already exist.</span></span>

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

### <span data-ttu-id="25d80-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="25d80-123">-SkuName</span></span>
<span data-ttu-id="25d80-124">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="25d80-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="25d80-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="25d80-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25d80-126">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="25d80-126">F0 (free tier)</span></span>
- <span data-ttu-id="25d80-127">S0</span><span class="sxs-lookup"><span data-stu-id="25d80-127">S0</span></span>
- <span data-ttu-id="25d80-128">Eles</span><span class="sxs-lookup"><span data-stu-id="25d80-128">S1</span></span>
- <span data-ttu-id="25d80-129">S2</span><span class="sxs-lookup"><span data-stu-id="25d80-129">S2</span></span>
- <span data-ttu-id="25d80-130">S3</span><span class="sxs-lookup"><span data-stu-id="25d80-130">S3</span></span>
- <span data-ttu-id="25d80-131">S4 para obter mais informações, consulte [APIs de serviço cognitiva](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="25d80-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="25d80-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="25d80-132">-Tag</span></span>
<span data-ttu-id="25d80-133">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="25d80-133">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="25d80-134">-Digite</span><span class="sxs-lookup"><span data-stu-id="25d80-134">-Type</span></span>
<span data-ttu-id="25d80-135">Especifica o tipo de conta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="25d80-135">Specifies the type of account to create.</span></span> <span data-ttu-id="25d80-136">Use o `Get-AzCognitiveServicesAccountType` cmdlet para obter os valores aceitáveis atuais.</span><span class="sxs-lookup"><span data-stu-id="25d80-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="25d80-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25d80-137">-Confirm</span></span>
<span data-ttu-id="25d80-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d80-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d80-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d80-139">-WhatIf</span></span>
<span data-ttu-id="25d80-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25d80-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d80-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25d80-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d80-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d80-142">CommonParameters</span></span>
<span data-ttu-id="25d80-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d80-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d80-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d80-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d80-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25d80-145">INPUTS</span></span>

### <span data-ttu-id="25d80-146">System. String</span><span class="sxs-lookup"><span data-stu-id="25d80-146">System.String</span></span>

## <span data-ttu-id="25d80-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25d80-147">OUTPUTS</span></span>

### <span data-ttu-id="25d80-148">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="25d80-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="25d80-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25d80-149">NOTES</span></span>

## <span data-ttu-id="25d80-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25d80-150">RELATED LINKS</span></span>

[<span data-ttu-id="25d80-151">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="25d80-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="25d80-152">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="25d80-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="25d80-153">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="25d80-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
