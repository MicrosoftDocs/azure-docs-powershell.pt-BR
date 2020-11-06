---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440514"
---
# <span data-ttu-id="8d5c8-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d5c8-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="8d5c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5c8-103">Modifica uma conta.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d5c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d5c8-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d5c8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="8d5c8-106">O cmdlet **set-AzureRmCognitiveServicesAccount** modifica a SKU ou marca da conta de serviços cognitivas especificada.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="8d5c8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d5c8-107">EXAMPLES</span></span>

## <span data-ttu-id="8d5c8-108">OS</span><span class="sxs-lookup"><span data-stu-id="8d5c8-108">PARAMETERS</span></span>

### <span data-ttu-id="8d5c8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5c8-109">-DefaultProfile</span></span>
<span data-ttu-id="8d5c8-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8d5c8-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d5c8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8d5c8-111">-Force</span></span>
<span data-ttu-id="8d5c8-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d5c8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d5c8-113">-Name</span></span>
<span data-ttu-id="8d5c8-114">Especifica o nome da conta a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-114">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="8d5c8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5c8-115">-ResourceGroupName</span></span>
<span data-ttu-id="8d5c8-116">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="8d5c8-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8d5c8-117">-SkuName</span></span>
<span data-ttu-id="8d5c8-118">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="8d5c8-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8d5c8-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d5c8-120">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="8d5c8-120">F0 (free tier)</span></span>
- <span data-ttu-id="8d5c8-121">S0</span><span class="sxs-lookup"><span data-stu-id="8d5c8-121">S0</span></span>
- <span data-ttu-id="8d5c8-122">Eles</span><span class="sxs-lookup"><span data-stu-id="8d5c8-122">S1</span></span>
- <span data-ttu-id="8d5c8-123">S2</span><span class="sxs-lookup"><span data-stu-id="8d5c8-123">S2</span></span>
- <span data-ttu-id="8d5c8-124">S3</span><span class="sxs-lookup"><span data-stu-id="8d5c8-124">S3</span></span>
- <span data-ttu-id="8d5c8-125">S4</span><span class="sxs-lookup"><span data-stu-id="8d5c8-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5c8-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="8d5c8-126">-Tag</span></span>
<span data-ttu-id="8d5c8-127">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5c8-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d5c8-128">-Confirm</span></span>
<span data-ttu-id="8d5c8-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d5c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d5c8-130">-WhatIf</span></span>
<span data-ttu-id="8d5c8-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d5c8-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d5c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5c8-133">CommonParameters</span></span>
<span data-ttu-id="8d5c8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5c8-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5c8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5c8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d5c8-136">INPUTS</span></span>

### <span data-ttu-id="8d5c8-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8d5c8-137">None</span></span>
<span data-ttu-id="8d5c8-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8d5c8-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d5c8-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d5c8-139">OUTPUTS</span></span>

### <span data-ttu-id="8d5c8-140">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d5c8-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="8d5c8-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d5c8-141">NOTES</span></span>

## <span data-ttu-id="8d5c8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d5c8-142">RELATED LINKS</span></span>

[<span data-ttu-id="8d5c8-143">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d5c8-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="8d5c8-144">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d5c8-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="8d5c8-145">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d5c8-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
