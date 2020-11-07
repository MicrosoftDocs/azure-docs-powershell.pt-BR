---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776084"
---
# <span data-ttu-id="97617-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97617-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="97617-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97617-102">SYNOPSIS</span></span>
<span data-ttu-id="97617-103">Remove um plano do serviço de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="97617-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="97617-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97617-104">SYNTAX</span></span>

### <span data-ttu-id="97617-105">Eles</span><span class="sxs-lookup"><span data-stu-id="97617-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97617-106">S2</span><span class="sxs-lookup"><span data-stu-id="97617-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97617-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97617-107">DESCRIPTION</span></span>
<span data-ttu-id="97617-108">O cmdlet **Remove-AzAppServicePlan** remove um plano do serviço de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="97617-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="97617-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97617-109">EXAMPLES</span></span>

### <span data-ttu-id="97617-110">Exemplo 1: remover um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="97617-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="97617-111">Esse comando Remove o plano do serviço de aplicativo Azure chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="97617-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="97617-112">OS</span><span class="sxs-lookup"><span data-stu-id="97617-112">PARAMETERS</span></span>

### <span data-ttu-id="97617-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97617-113">-AppServicePlan</span></span>
<span data-ttu-id="97617-114">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="97617-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="97617-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97617-115">-DefaultProfile</span></span>
<span data-ttu-id="97617-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97617-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97617-117">-Force</span><span class="sxs-lookup"><span data-stu-id="97617-117">-Force</span></span>
<span data-ttu-id="97617-118">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="97617-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="97617-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="97617-119">-Name</span></span>
<span data-ttu-id="97617-120">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="97617-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="97617-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97617-121">-ResourceGroupName</span></span>
<span data-ttu-id="97617-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="97617-122">Resource Group Name</span></span>

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

### <span data-ttu-id="97617-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97617-123">-Confirm</span></span>
<span data-ttu-id="97617-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97617-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97617-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97617-125">-WhatIf</span></span>
<span data-ttu-id="97617-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97617-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97617-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97617-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97617-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97617-128">-AsJob</span></span>
<span data-ttu-id="97617-129">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="97617-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97617-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97617-130">CommonParameters</span></span>
<span data-ttu-id="97617-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97617-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97617-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97617-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97617-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97617-133">INPUTS</span></span>

### <span data-ttu-id="97617-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="97617-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="97617-135">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="97617-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="97617-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97617-136">OUTPUTS</span></span>

### <span data-ttu-id="97617-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="97617-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="97617-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97617-138">NOTES</span></span>

## <span data-ttu-id="97617-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97617-139">RELATED LINKS</span></span>

[<span data-ttu-id="97617-140">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97617-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="97617-141">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97617-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="97617-142">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97617-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


