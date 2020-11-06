---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 05ee02fcb1a1f03c2a9b349754009a178a1668b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432367"
---
# <span data-ttu-id="7ae1e-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ae1e-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="7ae1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ae1e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae1e-103">Cria um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ae1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ae1e-104">SYNTAX</span></span>

### <span data-ttu-id="7ae1e-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ae1e-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ae1e-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ae1e-106">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ae1e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ae1e-107">DESCRIPTION</span></span>
<span data-ttu-id="7ae1e-108">O cmdlet **New-AzureRmWebApp** cria um aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="7ae1e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ae1e-109">EXAMPLES</span></span>

### <span data-ttu-id="7ae1e-110">Exemplo 1: criar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="7ae1e-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="7ae1e-111">Esse comando cria um aplicativo Web do Azure chamado ContosoSite no grupo de recursos existente chamado Default-Web-Oesteus no centro de dados West US.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="7ae1e-112">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="7ae1e-113">OS</span><span class="sxs-lookup"><span data-stu-id="7ae1e-113">PARAMETERS</span></span>

### <span data-ttu-id="7ae1e-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7ae1e-114">-AppServicePlan</span></span>
<span data-ttu-id="7ae1e-115">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7ae1e-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="7ae1e-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="7ae1e-117">Configurações do aplicativo substitui HashTable</span><span class="sxs-lookup"><span data-stu-id="7ae1e-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="7ae1e-118">-AseName</span></span>
<span data-ttu-id="7ae1e-119">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7ae1e-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae1e-120">-AseResourceGroupName</span></span>
<span data-ttu-id="7ae1e-121">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7ae1e-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ae1e-122">-AsJob</span></span>
<span data-ttu-id="7ae1e-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7ae1e-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ae1e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae1e-124">-DefaultProfile</span></span>
<span data-ttu-id="7ae1e-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ae1e-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="7ae1e-126">-GitRepositoryPath</span></span>
<span data-ttu-id="7ae1e-127">Caminho para o repositório GitHub containign o aplicativo Web a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="7ae1e-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="7ae1e-129">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="7ae1e-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="7ae1e-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="7ae1e-131">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="7ae1e-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="7ae1e-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="7ae1e-133">Opção incluir slots do WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="7ae1e-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-134">-Local</span><span class="sxs-lookup"><span data-stu-id="7ae1e-134">-Location</span></span>
<span data-ttu-id="7ae1e-135">Ponto</span><span class="sxs-lookup"><span data-stu-id="7ae1e-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ae1e-136">-Name</span></span>
<span data-ttu-id="7ae1e-137">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="7ae1e-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae1e-138">-ResourceGroupName</span></span>
<span data-ttu-id="7ae1e-139">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7ae1e-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="7ae1e-140">-SourceWebApp</span></span>
<span data-ttu-id="7ae1e-141">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="7ae1e-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7ae1e-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="7ae1e-143">ID do recurso do perfil do Gerenciador de tráfego existente</span><span class="sxs-lookup"><span data-stu-id="7ae1e-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ae1e-144">-Confirm</span></span>
<span data-ttu-id="7ae1e-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae1e-146">-WhatIf</span></span>
<span data-ttu-id="7ae1e-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ae1e-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae1e-149">CommonParameters</span></span>
<span data-ttu-id="7ae1e-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae1e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae1e-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae1e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae1e-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ae1e-152">INPUTS</span></span>

### <span data-ttu-id="7ae1e-153">Instalação</span><span class="sxs-lookup"><span data-stu-id="7ae1e-153">Site</span></span>
<span data-ttu-id="7ae1e-154">O parâmetro ' SourceWebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="7ae1e-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7ae1e-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ae1e-155">OUTPUTS</span></span>

### <span data-ttu-id="7ae1e-156">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="7ae1e-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="7ae1e-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ae1e-157">NOTES</span></span>

## <span data-ttu-id="7ae1e-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ae1e-158">RELATED LINKS</span></span>

[<span data-ttu-id="7ae1e-159">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ae1e-159">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="7ae1e-160">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ae1e-160">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="7ae1e-161">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ae1e-161">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="7ae1e-162">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ae1e-162">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="7ae1e-163">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ae1e-163">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)

