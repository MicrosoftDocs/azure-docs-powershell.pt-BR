---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440924"
---
# <span data-ttu-id="69319-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69319-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="69319-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69319-102">SYNOPSIS</span></span>
<span data-ttu-id="69319-103">Cria um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="69319-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69319-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69319-104">SYNTAX</span></span>

### <span data-ttu-id="69319-105">S1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="69319-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69319-106">S2</span><span class="sxs-lookup"><span data-stu-id="69319-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69319-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69319-107">DESCRIPTION</span></span>
<span data-ttu-id="69319-108">O cmdlet **New-AzureRmWebApp** cria um aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="69319-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="69319-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69319-109">EXAMPLES</span></span>

### <span data-ttu-id="69319-110">Exemplo 1: criar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="69319-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="69319-111">Esse comando cria um aplicativo Web do Azure chamado ContosoSite no grupo de recursos existente chamado Default-Web-Oesteus no centro de dados West US.</span><span class="sxs-lookup"><span data-stu-id="69319-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="69319-112">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="69319-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="69319-113">OS</span><span class="sxs-lookup"><span data-stu-id="69319-113">PARAMETERS</span></span>

### <span data-ttu-id="69319-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69319-114">-AppServicePlan</span></span>
<span data-ttu-id="69319-115">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="69319-115">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="69319-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="69319-117">Configurações do aplicativo substitui HashTable</span><span class="sxs-lookup"><span data-stu-id="69319-117">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="69319-118">-AseName</span></span>
<span data-ttu-id="69319-119">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="69319-119">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69319-120">-AseResourceGroupName</span></span>
<span data-ttu-id="69319-121">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="69319-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="69319-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="69319-123">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="69319-123">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="69319-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="69319-125">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="69319-125">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="69319-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="69319-127">Opção incluir slots do WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="69319-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-128">-Local</span><span class="sxs-lookup"><span data-stu-id="69319-128">-Location</span></span>
<span data-ttu-id="69319-129">Ponto</span><span class="sxs-lookup"><span data-stu-id="69319-129">Location</span></span>

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

### <span data-ttu-id="69319-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="69319-130">-Name</span></span>
<span data-ttu-id="69319-131">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="69319-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69319-132">-ResourceGroupName</span></span>
<span data-ttu-id="69319-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69319-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="69319-134">-SourceWebApp</span></span>
<span data-ttu-id="69319-135">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="69319-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69319-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="69319-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="69319-137">ID do perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="69319-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="69319-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="69319-139">Nome do perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="69319-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69319-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69319-140">-DefaultProfile</span></span>
<span data-ttu-id="69319-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69319-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69319-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69319-142">CommonParameters</span></span>
<span data-ttu-id="69319-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69319-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69319-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69319-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69319-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69319-145">INPUTS</span></span>

### <span data-ttu-id="69319-146">Instalação</span><span class="sxs-lookup"><span data-stu-id="69319-146">Site</span></span>
<span data-ttu-id="69319-147">O parâmetro ' SourceWebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="69319-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="69319-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69319-148">OUTPUTS</span></span>

## <span data-ttu-id="69319-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69319-149">NOTES</span></span>

## <span data-ttu-id="69319-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69319-150">RELATED LINKS</span></span>

[<span data-ttu-id="69319-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69319-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="69319-152">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69319-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="69319-153">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69319-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="69319-154">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69319-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="69319-155">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69319-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


