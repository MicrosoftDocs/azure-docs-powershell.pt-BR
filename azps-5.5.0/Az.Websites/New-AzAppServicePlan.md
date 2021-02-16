---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 863a1b42a6decd6b979516d21c007a9626e36d23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118501"
---
# <span data-ttu-id="c7964-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7964-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="c7964-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7964-102">SYNOPSIS</span></span>
<span data-ttu-id="c7964-103">Cria um plano de Serviço de Aplicativo do Azure em um determinado local geo.</span><span class="sxs-lookup"><span data-stu-id="c7964-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="c7964-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7964-104">SYNTAX</span></span>

### <span data-ttu-id="c7964-105">S1</span><span class="sxs-lookup"><span data-stu-id="c7964-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7964-106">S2</span><span class="sxs-lookup"><span data-stu-id="c7964-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7964-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7964-107">DESCRIPTION</span></span>
<span data-ttu-id="c7964-108">O cmdlet **New-AzAppServicePlan** cria um plano de Serviço do Aplicativo do Azure em um determinado local Geo com o nível, o tamanho do trabalhador e o número de trabalhadores especificados.</span><span class="sxs-lookup"><span data-stu-id="c7964-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="c7964-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c7964-109">EXAMPLES</span></span>

### <span data-ttu-id="c7964-110">Exemplo 1: Criar um plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c7964-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="c7964-111">Esse comando cria um plano de Serviço de Aplicativo chamado ContosoASP no grupo de recursos chamado Default-Web-WestUS na localização geográfica oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="c7964-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="c7964-112">O comando especifica um Nível Básico e atribui dois trabalhadores pequenos.</span><span class="sxs-lookup"><span data-stu-id="c7964-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="c7964-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7964-113">PARAMETERS</span></span>

### <span data-ttu-id="c7964-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7964-114">-AppServicePlan</span></span>
<span data-ttu-id="c7964-115">Objeto de Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c7964-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="c7964-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="c7964-116">-AseName</span></span>
<span data-ttu-id="c7964-117">Nome do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c7964-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="c7964-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7964-118">-AseResourceGroupName</span></span>
<span data-ttu-id="c7964-119">Nome do grupo de recursos de ambiente de serviço de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c7964-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="c7964-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7964-120">-AsJob</span></span>
<span data-ttu-id="c7964-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c7964-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7964-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7964-122">-DefaultProfile</span></span>
<span data-ttu-id="c7964-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c7964-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7964-124">-HiperV</span><span class="sxs-lookup"><span data-stu-id="c7964-124">-HyperV</span></span>
<span data-ttu-id="c7964-125">Especifique isso, o Plano de Serviço de Aplicativo executará Contêineres do Windows</span><span class="sxs-lookup"><span data-stu-id="c7964-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="c7964-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="c7964-126">-Linux</span></span>
<span data-ttu-id="c7964-127">Especifique isso, o Plano de Serviço de Aplicativo executará Contêineres do Linux</span><span class="sxs-lookup"><span data-stu-id="c7964-127">Specify this, App Service Plan will run Linux Containers</span></span>

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

### <span data-ttu-id="c7964-128">-Local</span><span class="sxs-lookup"><span data-stu-id="c7964-128">-Location</span></span>
<span data-ttu-id="c7964-129">Localização</span><span class="sxs-lookup"><span data-stu-id="c7964-129">Location</span></span> 

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

### <span data-ttu-id="c7964-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7964-130">-Name</span></span>
<span data-ttu-id="c7964-131">Nome do Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c7964-131">App Service Plan Name</span></span>

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

### <span data-ttu-id="c7964-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="c7964-132">-NumberofWorkers</span></span>
<span data-ttu-id="c7964-133">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="c7964-133">Number Of Workers</span></span>

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

### <span data-ttu-id="c7964-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="c7964-134">-PerSiteScaling</span></span>
<span data-ttu-id="c7964-135">Se você quer ou não habilitar o Dimensionamento por Site</span><span class="sxs-lookup"><span data-stu-id="c7964-135">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="c7964-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7964-136">-ResourceGroupName</span></span>
<span data-ttu-id="c7964-137">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c7964-137">Resource Group Name</span></span>

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

### <span data-ttu-id="c7964-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7964-138">-Tag</span></span>
<span data-ttu-id="c7964-139">Marcas são pares de nome/valor que permitem categorizar recursos</span><span class="sxs-lookup"><span data-stu-id="c7964-139">Tags are name/value pairs that enable you to categorize resources</span></span>

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

### <span data-ttu-id="c7964-140">-Tier</span><span class="sxs-lookup"><span data-stu-id="c7964-140">-Tier</span></span>
<span data-ttu-id="c7964-141">Camada</span><span class="sxs-lookup"><span data-stu-id="c7964-141">Tier</span></span>

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

### <span data-ttu-id="c7964-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="c7964-142">-WorkerSize</span></span>
<span data-ttu-id="c7964-143">Tamanho do profissional da Web</span><span class="sxs-lookup"><span data-stu-id="c7964-143">Size of web worker</span></span>

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

### <span data-ttu-id="c7964-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7964-144">CommonParameters</span></span>
<span data-ttu-id="c7964-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7964-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7964-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7964-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7964-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="c7964-147">INPUTS</span></span>

### <span data-ttu-id="c7964-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7964-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="c7964-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="c7964-149">OUTPUTS</span></span>

### <span data-ttu-id="c7964-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7964-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="c7964-151">Notas</span><span class="sxs-lookup"><span data-stu-id="c7964-151">NOTES</span></span>

## <span data-ttu-id="c7964-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7964-152">RELATED LINKS</span></span>

[<span data-ttu-id="c7964-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7964-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="c7964-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7964-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="c7964-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7964-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


