---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112340"
---
# <span data-ttu-id="6c404-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6c404-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="6c404-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c404-102">SYNOPSIS</span></span>
<span data-ttu-id="6c404-103">Obtém um plano de Serviço de Aplicativo do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="6c404-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="6c404-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c404-104">SYNTAX</span></span>

### <span data-ttu-id="6c404-105">S1</span><span class="sxs-lookup"><span data-stu-id="6c404-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c404-106">S2</span><span class="sxs-lookup"><span data-stu-id="6c404-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c404-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c404-107">DESCRIPTION</span></span>
<span data-ttu-id="6c404-108">O **cmdlet Get-AzAppServicePlan** obtém um plano do Serviço de Aplicativo do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="6c404-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="6c404-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c404-109">EXAMPLES</span></span>

### <span data-ttu-id="6c404-110">Exemplo 1: Obter um plano de Serviço de Aplicativo de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6c404-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="6c404-111">Esse comando obtém o plano serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6c404-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="6c404-112">Exemplo 2: Obter todos os planos do Serviço de Aplicativo em um local</span><span class="sxs-lookup"><span data-stu-id="6c404-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="6c404-113">Esse comando obtém todos os planos do Serviço de Aplicativo localizados na região "Oeste dos EUA".</span><span class="sxs-lookup"><span data-stu-id="6c404-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="6c404-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c404-114">PARAMETERS</span></span>

### <span data-ttu-id="6c404-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c404-115">-DefaultProfile</span></span>
<span data-ttu-id="6c404-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6c404-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c404-117">-Local</span><span class="sxs-lookup"><span data-stu-id="6c404-117">-Location</span></span>
<span data-ttu-id="6c404-118">Localização</span><span class="sxs-lookup"><span data-stu-id="6c404-118">Location</span></span> 

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

### <span data-ttu-id="6c404-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c404-119">-Name</span></span>
<span data-ttu-id="6c404-120">Nome do Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6c404-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="6c404-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c404-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c404-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6c404-122">Resource Group Name</span></span>

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

### <span data-ttu-id="6c404-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c404-123">CommonParameters</span></span>
<span data-ttu-id="6c404-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c404-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c404-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c404-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c404-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="6c404-126">INPUTS</span></span>

### <span data-ttu-id="6c404-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6c404-127">None</span></span>

## <span data-ttu-id="6c404-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="6c404-128">OUTPUTS</span></span>

### <span data-ttu-id="6c404-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6c404-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="6c404-130">Notas</span><span class="sxs-lookup"><span data-stu-id="6c404-130">NOTES</span></span>

## <span data-ttu-id="6c404-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c404-131">RELATED LINKS</span></span>

[<span data-ttu-id="6c404-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6c404-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="6c404-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6c404-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="6c404-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6c404-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


