---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 9a1c1de8aef41089cfc874cf35b26fcc9bf0be52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893043"
---
# <span data-ttu-id="b8d4a-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8d4a-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="b8d4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d4a-103">Cria um plano de Serviço de Aplicativo do Azure em um determinado local Geo.</span><span class="sxs-lookup"><span data-stu-id="b8d4a-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="b8d4a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8d4a-104">SYNTAX</span></span>

### <span data-ttu-id="b8d4a-105">S1</span><span class="sxs-lookup"><span data-stu-id="b8d4a-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8d4a-106">S2</span><span class="sxs-lookup"><span data-stu-id="b8d4a-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8d4a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8d4a-107">DESCRIPTION</span></span>
<span data-ttu-id="b8d4a-108">O cmdlet **New-AzAppServicePlan** cria um plano de Serviço de Aplicativo do Azure em uma determinada localização Geográfica com a Camada especificada, o tamanho do trabalho e o número de funcionários.</span><span class="sxs-lookup"><span data-stu-id="b8d4a-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="b8d4a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8d4a-109">EXAMPLES</span></span>

### <span data-ttu-id="b8d4a-110">Exemplo 1: Criar um plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="b8d4a-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="b8d4a-111">Este comando cria um plano de Serviço de Aplicativo chamado ContosoASP no grupo de recursos chamado Default-Web-WestUS na localização geográfica do Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="b8d4a-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="b8d4a-112">O comando especifica uma Camada Básica e aloca dois pequenos funcionários.</span><span class="sxs-lookup"><span data-stu-id="b8d4a-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="b8d4a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8d4a-113">PARAMETERS</span></span>

### <span data-ttu-id="b8d4a-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8d4a-114">-AppServicePlan</span></span>
<span data-ttu-id="b8d4a-115">Objeto Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="b8d4a-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="b8d4a-116">-AseName</span></span>
<span data-ttu-id="b8d4a-117">Nome do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b8d4a-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d4a-118">-AseResourceGroupName</span></span>
<span data-ttu-id="b8d4a-119">Nome do grupo de recursos do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b8d4a-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8d4a-120">-AsJob</span></span>
<span data-ttu-id="b8d4a-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b8d4a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8d4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d4a-122">-DefaultProfile</span></span>
<span data-ttu-id="b8d4a-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b8d4a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8d4a-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="b8d4a-124">-HyperV</span></span>
<span data-ttu-id="b8d4a-125">Especifique isso, o Plano de Serviço de Aplicativo executará Contêineres do Windows</span><span class="sxs-lookup"><span data-stu-id="b8d4a-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="b8d4a-126">-Linux</span></span>
<span data-ttu-id="b8d4a-127">Especifique isso, o Plano de Serviço de Aplicativo executará Contêineres Linux</span><span class="sxs-lookup"><span data-stu-id="b8d4a-127">Specify this, App Service Plan will run Linux Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-128">-Location</span><span class="sxs-lookup"><span data-stu-id="b8d4a-128">-Location</span></span>
<span data-ttu-id="b8d4a-129">Local</span><span class="sxs-lookup"><span data-stu-id="b8d4a-129">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b8d4a-130">-Name</span></span>
<span data-ttu-id="b8d4a-131">Nome do Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="b8d4a-131">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="b8d4a-132">-NumberofWorkers</span></span>
<span data-ttu-id="b8d4a-133">Número de funcionários</span><span class="sxs-lookup"><span data-stu-id="b8d4a-133">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="b8d4a-134">-PerSiteScaling</span></span>
<span data-ttu-id="b8d4a-135">Se deve ou não habilitar o Dimensionamento por Site</span><span class="sxs-lookup"><span data-stu-id="b8d4a-135">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d4a-136">-ResourceGroupName</span></span>
<span data-ttu-id="b8d4a-137">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b8d4a-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8d4a-138">-Tag</span></span>
<span data-ttu-id="b8d4a-139">Marcas são pares de nome/valor que permitem categorizar recursos</span><span class="sxs-lookup"><span data-stu-id="b8d4a-139">Tags are name/value pairs that enable you to categorize resources</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-140">-Tier</span><span class="sxs-lookup"><span data-stu-id="b8d4a-140">-Tier</span></span>
<span data-ttu-id="b8d4a-141">Camada</span><span class="sxs-lookup"><span data-stu-id="b8d4a-141">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="b8d4a-142">-WorkerSize</span></span>
<span data-ttu-id="b8d4a-143">Tamanho do trabalhador da Web</span><span class="sxs-lookup"><span data-stu-id="b8d4a-143">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d4a-144">CommonParameters</span></span>
<span data-ttu-id="b8d4a-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d4a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d4a-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8d4a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d4a-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8d4a-147">INPUTS</span></span>

### <span data-ttu-id="b8d4a-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8d4a-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b8d4a-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8d4a-149">OUTPUTS</span></span>

### <span data-ttu-id="b8d4a-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8d4a-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b8d4a-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8d4a-151">NOTES</span></span>

## <span data-ttu-id="b8d4a-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8d4a-152">RELATED LINKS</span></span>

[<span data-ttu-id="b8d4a-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8d4a-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="b8d4a-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8d4a-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="b8d4a-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8d4a-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


