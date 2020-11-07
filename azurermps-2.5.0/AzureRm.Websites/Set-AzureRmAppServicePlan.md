---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: eac153c22a576686feb15b75f3180ed4fb12ec94
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786198"
---
# <span data-ttu-id="cb5f0-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cb5f0-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="cb5f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5f0-103">Define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb5f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb5f0-104">SYNTAX</span></span>

### <span data-ttu-id="cb5f0-105">Eles</span><span class="sxs-lookup"><span data-stu-id="cb5f0-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb5f0-106">S2</span><span class="sxs-lookup"><span data-stu-id="cb5f0-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb5f0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb5f0-107">DESCRIPTION</span></span>
<span data-ttu-id="cb5f0-108">O cmdlet **set-AzureRmAppServicePlan** define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="cb5f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb5f0-109">EXAMPLES</span></span>

### <span data-ttu-id="cb5f0-110">1: modificar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb5f0-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="cb5f0-111">Esse comando define a opção PerSiteScaling como true no plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="cb5f0-112">OS</span><span class="sxs-lookup"><span data-stu-id="cb5f0-112">PARAMETERS</span></span>

### <span data-ttu-id="cb5f0-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="cb5f0-113">-AdminSiteName</span></span>
<span data-ttu-id="cb5f0-114">Nome do site de administração</span><span class="sxs-lookup"><span data-stu-id="cb5f0-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5f0-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cb5f0-115">-AppServicePlan</span></span>
<span data-ttu-id="cb5f0-116">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb5f0-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="cb5f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5f0-117">-DefaultProfile</span></span>
<span data-ttu-id="cb5f0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb5f0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb5f0-119">-Name</span></span>
<span data-ttu-id="cb5f0-120">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb5f0-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="cb5f0-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="cb5f0-121">-NumberofWorkers</span></span>
<span data-ttu-id="cb5f0-122">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="cb5f0-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5f0-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="cb5f0-123">-PerSiteScaling</span></span>
<span data-ttu-id="cb5f0-124">Booleano de dimensionamento por site</span><span class="sxs-lookup"><span data-stu-id="cb5f0-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb5f0-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cb5f0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cb5f0-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="cb5f0-127">-Tier</span></span>
<span data-ttu-id="cb5f0-128">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="cb5f0-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5f0-129">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="cb5f0-129">-WorkerSize</span></span>
<span data-ttu-id="cb5f0-130">Tamanho do trabalhador</span><span class="sxs-lookup"><span data-stu-id="cb5f0-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="cb5f0-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb5f0-131">-AsJob</span></span>
<span data-ttu-id="cb5f0-132">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cb5f0-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb5f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5f0-133">CommonParameters</span></span>
<span data-ttu-id="cb5f0-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5f0-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb5f0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5f0-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb5f0-136">INPUTS</span></span>

### <span data-ttu-id="cb5f0-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="cb5f0-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="cb5f0-138">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cb5f0-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="cb5f0-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb5f0-139">OUTPUTS</span></span>

### <span data-ttu-id="cb5f0-140">Microsoft. Azure. Management. WebSites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="cb5f0-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="cb5f0-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb5f0-141">NOTES</span></span>

## <span data-ttu-id="cb5f0-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb5f0-142">RELATED LINKS</span></span>

[<span data-ttu-id="cb5f0-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="cb5f0-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="cb5f0-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="cb5f0-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="cb5f0-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="cb5f0-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="cb5f0-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="cb5f0-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="cb5f0-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="cb5f0-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="cb5f0-148">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="cb5f0-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


