---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: d19c22ffd0be5b6ea935b832d847bb74661e3106
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597542"
---
# <span data-ttu-id="fc16b-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fc16b-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="fc16b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc16b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc16b-103">Cria uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="fc16b-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="fc16b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc16b-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc16b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc16b-105">DESCRIPTION</span></span>
<span data-ttu-id="fc16b-106">O cmdlet **New-AzCognitiveServicesAccount** cria uma conta de serviços cognitivas com o tipo e a SKU especificados.</span><span class="sxs-lookup"><span data-stu-id="fc16b-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="fc16b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc16b-107">EXAMPLES</span></span>

### <span data-ttu-id="fc16b-108">1:</span><span class="sxs-lookup"><span data-stu-id="fc16b-108">1:</span></span>
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

## <span data-ttu-id="fc16b-109">OS</span><span class="sxs-lookup"><span data-stu-id="fc16b-109">PARAMETERS</span></span>

### <span data-ttu-id="fc16b-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="fc16b-110">-CustomSubdomainName</span></span>
<span data-ttu-id="fc16b-111">Nome de subdomínio da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="fc16b-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="fc16b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc16b-112">-DefaultProfile</span></span>
<span data-ttu-id="fc16b-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fc16b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc16b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fc16b-114">-Force</span></span>
<span data-ttu-id="fc16b-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc16b-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc16b-116">-Local</span><span class="sxs-lookup"><span data-stu-id="fc16b-116">-Location</span></span>
<span data-ttu-id="fc16b-117">Especifica o local no qual criar a conta.</span><span class="sxs-lookup"><span data-stu-id="fc16b-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="fc16b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc16b-118">-Name</span></span>
<span data-ttu-id="fc16b-119">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="fc16b-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="fc16b-120">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc16b-120">-NetworkRuleSet</span></span>
<span data-ttu-id="fc16b-121">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como manipular solicitações que não correspondem a nenhuma das regras definidas</span><span class="sxs-lookup"><span data-stu-id="fc16b-121">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc16b-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc16b-123">Especifica o nome do grupo de recursos ao qual a conta será atribuída.</span><span class="sxs-lookup"><span data-stu-id="fc16b-123">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="fc16b-124">O grupo de recursos já deve existir.</span><span class="sxs-lookup"><span data-stu-id="fc16b-124">The resource group must already exist.</span></span>

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

### <span data-ttu-id="fc16b-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fc16b-125">-SkuName</span></span>
<span data-ttu-id="fc16b-126">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="fc16b-126">Specifies the SKU for the account.</span></span>
<span data-ttu-id="fc16b-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fc16b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc16b-128">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="fc16b-128">F0 (free tier)</span></span>
- <span data-ttu-id="fc16b-129">S0</span><span class="sxs-lookup"><span data-stu-id="fc16b-129">S0</span></span>
- <span data-ttu-id="fc16b-130">Eles</span><span class="sxs-lookup"><span data-stu-id="fc16b-130">S1</span></span>
- <span data-ttu-id="fc16b-131">S2</span><span class="sxs-lookup"><span data-stu-id="fc16b-131">S2</span></span>
- <span data-ttu-id="fc16b-132">S3</span><span class="sxs-lookup"><span data-stu-id="fc16b-132">S3</span></span>
- <span data-ttu-id="fc16b-133">S4 para obter mais informações, consulte [APIs de serviço cognitiva](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="fc16b-133">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="fc16b-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="fc16b-134">-Tag</span></span>
<span data-ttu-id="fc16b-135">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="fc16b-135">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="fc16b-136">-Digite</span><span class="sxs-lookup"><span data-stu-id="fc16b-136">-Type</span></span>
<span data-ttu-id="fc16b-137">Especifica o tipo de conta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="fc16b-137">Specifies the type of account to create.</span></span> <span data-ttu-id="fc16b-138">Use o `Get-AzCognitiveServicesAccountType` cmdlet para obter os valores aceitáveis atuais.</span><span class="sxs-lookup"><span data-stu-id="fc16b-138">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="fc16b-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc16b-139">-Confirm</span></span>
<span data-ttu-id="fc16b-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc16b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc16b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc16b-141">-WhatIf</span></span>
<span data-ttu-id="fc16b-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc16b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc16b-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc16b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc16b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc16b-144">CommonParameters</span></span>
<span data-ttu-id="fc16b-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc16b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc16b-146">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc16b-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc16b-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc16b-147">INPUTS</span></span>

### <span data-ttu-id="fc16b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="fc16b-148">System.String</span></span>

## <span data-ttu-id="fc16b-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc16b-149">OUTPUTS</span></span>

### <span data-ttu-id="fc16b-150">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fc16b-150">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="fc16b-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc16b-151">NOTES</span></span>

## <span data-ttu-id="fc16b-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc16b-152">RELATED LINKS</span></span>

[<span data-ttu-id="fc16b-153">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fc16b-153">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="fc16b-154">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fc16b-154">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="fc16b-155">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fc16b-155">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
