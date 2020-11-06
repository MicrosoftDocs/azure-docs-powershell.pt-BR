---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 51338a2cae2aa8bde09ecdea18f0aa74f3727fef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441193"
---
# <span data-ttu-id="b9c14-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b9c14-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="b9c14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9c14-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c14-103">Modifica uma conta.</span><span class="sxs-lookup"><span data-stu-id="b9c14-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9c14-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c14-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9c14-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c14-106">O cmdlet **set-AzureRmCognitiveServicesAccount** modifica a SKU ou marca da conta de serviços cognitivas especificada.</span><span class="sxs-lookup"><span data-stu-id="b9c14-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="b9c14-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9c14-107">EXAMPLES</span></span>

## <span data-ttu-id="b9c14-108">OS</span><span class="sxs-lookup"><span data-stu-id="b9c14-108">PARAMETERS</span></span>

### <span data-ttu-id="b9c14-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b9c14-109">-Force</span></span>
<span data-ttu-id="b9c14-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b9c14-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9c14-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9c14-111">-Name</span></span>
<span data-ttu-id="b9c14-112">Especifica o nome da conta a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="b9c14-112">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="b9c14-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c14-113">-ResourceGroupName</span></span>
<span data-ttu-id="b9c14-114">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="b9c14-114">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="b9c14-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b9c14-115">-SkuName</span></span>
<span data-ttu-id="b9c14-116">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="b9c14-116">Specifies the SKU for the account.</span></span>
<span data-ttu-id="b9c14-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b9c14-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9c14-118">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="b9c14-118">F0 (free tier)</span></span>
- <span data-ttu-id="b9c14-119">S0</span><span class="sxs-lookup"><span data-stu-id="b9c14-119">S0</span></span>
- <span data-ttu-id="b9c14-120">Eles</span><span class="sxs-lookup"><span data-stu-id="b9c14-120">S1</span></span>
- <span data-ttu-id="b9c14-121">S2</span><span class="sxs-lookup"><span data-stu-id="b9c14-121">S2</span></span>
- <span data-ttu-id="b9c14-122">S3</span><span class="sxs-lookup"><span data-stu-id="b9c14-122">S3</span></span>
- <span data-ttu-id="b9c14-123">S4</span><span class="sxs-lookup"><span data-stu-id="b9c14-123">S4</span></span>

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

### <span data-ttu-id="b9c14-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="b9c14-124">-Tag</span></span>
<span data-ttu-id="b9c14-125">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="b9c14-125">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="b9c14-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9c14-126">-Confirm</span></span>
<span data-ttu-id="b9c14-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c14-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c14-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c14-128">-WhatIf</span></span>
<span data-ttu-id="b9c14-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9c14-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c14-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9c14-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c14-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c14-131">-DefaultProfile</span></span>
<span data-ttu-id="b9c14-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c14-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c14-133">CommonParameters</span></span>
<span data-ttu-id="b9c14-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c14-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c14-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c14-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9c14-136">INPUTS</span></span>

## <span data-ttu-id="b9c14-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9c14-137">OUTPUTS</span></span>

### <span data-ttu-id="b9c14-138">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b9c14-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="b9c14-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9c14-139">NOTES</span></span>

## <span data-ttu-id="b9c14-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9c14-140">RELATED LINKS</span></span>

[<span data-ttu-id="b9c14-141">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b9c14-141">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b9c14-142">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b9c14-142">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b9c14-143">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b9c14-143">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
