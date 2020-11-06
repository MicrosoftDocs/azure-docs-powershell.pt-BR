---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601387"
---
# <span data-ttu-id="fde01-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fde01-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="fde01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fde01-102">SYNOPSIS</span></span>
<span data-ttu-id="fde01-103">Modifica uma conta.</span><span class="sxs-lookup"><span data-stu-id="fde01-103">Modifies an account.</span></span>

## <span data-ttu-id="fde01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fde01-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fde01-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fde01-105">DESCRIPTION</span></span>
<span data-ttu-id="fde01-106">O cmdlet **set-AzCognitiveServicesAccount** modifica a SKU ou marca da conta de serviços cognitivas especificada.</span><span class="sxs-lookup"><span data-stu-id="fde01-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="fde01-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fde01-107">EXAMPLES</span></span>

### <span data-ttu-id="fde01-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fde01-108">Example 1</span></span>
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

## <span data-ttu-id="fde01-109">OS</span><span class="sxs-lookup"><span data-stu-id="fde01-109">PARAMETERS</span></span>

### <span data-ttu-id="fde01-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde01-110">-DefaultProfile</span></span>
<span data-ttu-id="fde01-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fde01-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fde01-112">-Force</span><span class="sxs-lookup"><span data-stu-id="fde01-112">-Force</span></span>
<span data-ttu-id="fde01-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fde01-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fde01-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="fde01-114">-Name</span></span>
<span data-ttu-id="fde01-115">Especifica o nome da conta a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="fde01-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="fde01-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde01-116">-ResourceGroupName</span></span>
<span data-ttu-id="fde01-117">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="fde01-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="fde01-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fde01-118">-SkuName</span></span>
<span data-ttu-id="fde01-119">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="fde01-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="fde01-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fde01-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fde01-121">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="fde01-121">F0 (free tier)</span></span>
- <span data-ttu-id="fde01-122">S0</span><span class="sxs-lookup"><span data-stu-id="fde01-122">S0</span></span>
- <span data-ttu-id="fde01-123">Eles</span><span class="sxs-lookup"><span data-stu-id="fde01-123">S1</span></span>
- <span data-ttu-id="fde01-124">S2</span><span class="sxs-lookup"><span data-stu-id="fde01-124">S2</span></span>
- <span data-ttu-id="fde01-125">S3</span><span class="sxs-lookup"><span data-stu-id="fde01-125">S3</span></span>
- <span data-ttu-id="fde01-126">S4</span><span class="sxs-lookup"><span data-stu-id="fde01-126">S4</span></span>

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

### <span data-ttu-id="fde01-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="fde01-127">-Tag</span></span>
<span data-ttu-id="fde01-128">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="fde01-128">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="fde01-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fde01-129">-Confirm</span></span>
<span data-ttu-id="fde01-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fde01-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fde01-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde01-131">-WhatIf</span></span>
<span data-ttu-id="fde01-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fde01-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fde01-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fde01-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fde01-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde01-134">CommonParameters</span></span>
<span data-ttu-id="fde01-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde01-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde01-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde01-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde01-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fde01-137">INPUTS</span></span>

### <span data-ttu-id="fde01-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fde01-138">System.String</span></span>

### <span data-ttu-id="fde01-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="fde01-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="fde01-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fde01-140">OUTPUTS</span></span>

### <span data-ttu-id="fde01-141">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fde01-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="fde01-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fde01-142">NOTES</span></span>

## <span data-ttu-id="fde01-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fde01-143">RELATED LINKS</span></span>

[<span data-ttu-id="fde01-144">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fde01-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="fde01-145">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fde01-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="fde01-146">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fde01-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
