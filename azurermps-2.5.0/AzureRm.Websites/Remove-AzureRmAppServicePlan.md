---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: e8ce0397a59a72e2960a8e0af978c1b5484c53af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785136"
---
# <span data-ttu-id="d79d0-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d79d0-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="d79d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d79d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d79d0-103">Remove um plano do serviço de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d79d0-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d79d0-104">SYNTAX</span></span>

### <span data-ttu-id="d79d0-105">Eles</span><span class="sxs-lookup"><span data-stu-id="d79d0-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d79d0-106">S2</span><span class="sxs-lookup"><span data-stu-id="d79d0-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d79d0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d79d0-107">DESCRIPTION</span></span>
<span data-ttu-id="d79d0-108">O cmdlet **Remove-AzureRmAppServicePlan** remove um plano do serviço de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d79d0-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="d79d0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d79d0-109">EXAMPLES</span></span>

### <span data-ttu-id="d79d0-110">Exemplo 1: remover um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d79d0-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="d79d0-111">Esse comando Remove o plano do serviço de aplicativo Azure chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="d79d0-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d79d0-112">OS</span><span class="sxs-lookup"><span data-stu-id="d79d0-112">PARAMETERS</span></span>

### <span data-ttu-id="d79d0-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d79d0-113">-AppServicePlan</span></span>
<span data-ttu-id="d79d0-114">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d79d0-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d79d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79d0-115">-DefaultProfile</span></span>
<span data-ttu-id="d79d0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d79d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d79d0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d79d0-117">-Force</span></span>
<span data-ttu-id="d79d0-118">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="d79d0-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d79d0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d79d0-119">-Name</span></span>
<span data-ttu-id="d79d0-120">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d79d0-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="d79d0-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d79d0-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79d0-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d79d0-123">-Confirm</span></span>
<span data-ttu-id="d79d0-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d79d0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d79d0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79d0-125">-WhatIf</span></span>
<span data-ttu-id="d79d0-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d79d0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79d0-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d79d0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d79d0-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d79d0-128">-AsJob</span></span>
<span data-ttu-id="d79d0-129">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d79d0-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d79d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79d0-130">CommonParameters</span></span>
<span data-ttu-id="d79d0-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d79d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79d0-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79d0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79d0-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d79d0-133">INPUTS</span></span>

### <span data-ttu-id="d79d0-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="d79d0-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="d79d0-135">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d79d0-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="d79d0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d79d0-136">OUTPUTS</span></span>

### <span data-ttu-id="d79d0-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d79d0-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d79d0-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d79d0-138">NOTES</span></span>

## <span data-ttu-id="d79d0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d79d0-139">RELATED LINKS</span></span>

[<span data-ttu-id="d79d0-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d79d0-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="d79d0-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d79d0-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="d79d0-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d79d0-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


