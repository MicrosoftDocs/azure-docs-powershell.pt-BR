---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 57d136691d6ca0ac9bcd85f205d70cf267437b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597533"
---
# <span data-ttu-id="bb218-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb218-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="bb218-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb218-102">SYNOPSIS</span></span>
<span data-ttu-id="bb218-103">Modifica uma conta.</span><span class="sxs-lookup"><span data-stu-id="bb218-103">Modifies an account.</span></span>

## <span data-ttu-id="bb218-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb218-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb218-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb218-105">DESCRIPTION</span></span>
<span data-ttu-id="bb218-106">O cmdlet **set-AzCognitiveServicesAccount** modifica a SKU ou marca da conta de serviços cognitivas especificada.</span><span class="sxs-lookup"><span data-stu-id="bb218-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="bb218-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb218-107">EXAMPLES</span></span>

### <span data-ttu-id="bb218-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb218-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="bb218-109">OS</span><span class="sxs-lookup"><span data-stu-id="bb218-109">PARAMETERS</span></span>

### <span data-ttu-id="bb218-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="bb218-110">-CustomSubdomainName</span></span>
<span data-ttu-id="bb218-111">Nome de subdomínio da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="bb218-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="bb218-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb218-112">-DefaultProfile</span></span>
<span data-ttu-id="bb218-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bb218-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb218-114">-Force</span><span class="sxs-lookup"><span data-stu-id="bb218-114">-Force</span></span>
<span data-ttu-id="bb218-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bb218-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bb218-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb218-116">-Name</span></span>
<span data-ttu-id="bb218-117">Especifica o nome da conta a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="bb218-117">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="bb218-118">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bb218-118">-NetworkRuleSet</span></span>
<span data-ttu-id="bb218-119">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como manipular solicitações que não correspondem a nenhuma das regras definidas</span><span class="sxs-lookup"><span data-stu-id="bb218-119">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="bb218-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb218-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb218-121">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="bb218-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="bb218-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bb218-122">-SkuName</span></span>
<span data-ttu-id="bb218-123">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="bb218-123">Specifies the SKU for the account.</span></span>
<span data-ttu-id="bb218-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bb218-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb218-125">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="bb218-125">F0 (free tier)</span></span>
- <span data-ttu-id="bb218-126">S0</span><span class="sxs-lookup"><span data-stu-id="bb218-126">S0</span></span>
- <span data-ttu-id="bb218-127">Eles</span><span class="sxs-lookup"><span data-stu-id="bb218-127">S1</span></span>
- <span data-ttu-id="bb218-128">S2</span><span class="sxs-lookup"><span data-stu-id="bb218-128">S2</span></span>
- <span data-ttu-id="bb218-129">S3</span><span class="sxs-lookup"><span data-stu-id="bb218-129">S3</span></span>
- <span data-ttu-id="bb218-130">S4</span><span class="sxs-lookup"><span data-stu-id="bb218-130">S4</span></span>

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

### <span data-ttu-id="bb218-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="bb218-131">-Tag</span></span>
<span data-ttu-id="bb218-132">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="bb218-132">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="bb218-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb218-133">-Confirm</span></span>
<span data-ttu-id="bb218-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb218-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb218-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb218-135">-WhatIf</span></span>
<span data-ttu-id="bb218-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb218-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb218-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb218-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb218-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb218-138">CommonParameters</span></span>
<span data-ttu-id="bb218-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb218-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb218-140">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb218-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb218-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb218-141">INPUTS</span></span>

### <span data-ttu-id="bb218-142">System. String</span><span class="sxs-lookup"><span data-stu-id="bb218-142">System.String</span></span>

### <span data-ttu-id="bb218-143">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="bb218-143">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="bb218-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb218-144">OUTPUTS</span></span>

### <span data-ttu-id="bb218-145">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb218-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="bb218-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb218-146">NOTES</span></span>

## <span data-ttu-id="bb218-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb218-147">RELATED LINKS</span></span>

[<span data-ttu-id="bb218-148">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb218-148">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="bb218-149">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb218-149">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="bb218-150">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb218-150">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
