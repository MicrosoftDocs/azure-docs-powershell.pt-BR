---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777610"
---
# <span data-ttu-id="e5c3d-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5c3d-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="e5c3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c3d-103">Obtém um plano do serviço de aplicativo do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e5c3d-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="e5c3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5c3d-104">SYNTAX</span></span>

### <span data-ttu-id="e5c3d-105">Eles</span><span class="sxs-lookup"><span data-stu-id="e5c3d-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c3d-106">S2</span><span class="sxs-lookup"><span data-stu-id="e5c3d-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c3d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5c3d-107">DESCRIPTION</span></span>
<span data-ttu-id="e5c3d-108">O cmdlet **Get-AzAppServicePlan** Obtém um plano do serviço de aplicativo do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e5c3d-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="e5c3d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5c3d-109">EXAMPLES</span></span>

### <span data-ttu-id="e5c3d-110">Exemplo 1: obter um plano do serviço de aplicativo de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e5c3d-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="e5c3d-111">Esse comando obtém o plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="e5c3d-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="e5c3d-112">Exemplo 2: obter todos os planos do serviço de aplicativo em um local</span><span class="sxs-lookup"><span data-stu-id="e5c3d-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="e5c3d-113">Esse comando obtém todos os planos do serviço de aplicativo localizado na região "oeste dos EUA".</span><span class="sxs-lookup"><span data-stu-id="e5c3d-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="e5c3d-114">OS</span><span class="sxs-lookup"><span data-stu-id="e5c3d-114">PARAMETERS</span></span>

### <span data-ttu-id="e5c3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c3d-115">-DefaultProfile</span></span>
<span data-ttu-id="e5c3d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c3d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c3d-117">-Local</span><span class="sxs-lookup"><span data-stu-id="e5c3d-117">-Location</span></span>
<span data-ttu-id="e5c3d-118">Ponto</span><span class="sxs-lookup"><span data-stu-id="e5c3d-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c3d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5c3d-119">-Name</span></span>
<span data-ttu-id="e5c3d-120">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e5c3d-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c3d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c3d-121">-ResourceGroupName</span></span>
<span data-ttu-id="e5c3d-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e5c3d-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c3d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c3d-123">CommonParameters</span></span>
<span data-ttu-id="e5c3d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c3d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c3d-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c3d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c3d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5c3d-126">INPUTS</span></span>

### <span data-ttu-id="e5c3d-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e5c3d-127">None</span></span>

## <span data-ttu-id="e5c3d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5c3d-128">OUTPUTS</span></span>

### <span data-ttu-id="e5c3d-129">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5c3d-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="e5c3d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5c3d-130">NOTES</span></span>

## <span data-ttu-id="e5c3d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5c3d-131">RELATED LINKS</span></span>

[<span data-ttu-id="e5c3d-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5c3d-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="e5c3d-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5c3d-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="e5c3d-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5c3d-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


