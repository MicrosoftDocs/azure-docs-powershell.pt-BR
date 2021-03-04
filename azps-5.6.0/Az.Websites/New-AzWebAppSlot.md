---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 283b3dd7ec57150d1c93a6e01a85251ed94fbdf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888018"
---
# <span data-ttu-id="81700-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81700-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="81700-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81700-102">SYNOPSIS</span></span>
<span data-ttu-id="81700-103">Cria um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="81700-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="81700-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="81700-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81700-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="81700-105">DESCRIPTION</span></span>
<span data-ttu-id="81700-106">O cmdlet **New-AzWebAppSlot** cria um Slot do Aplicativo Web do Azure em um determinado grupo de recursos que usa o plano de Serviço de Aplicativo especificado e o data center.</span><span class="sxs-lookup"><span data-stu-id="81700-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="81700-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81700-107">EXAMPLES</span></span>

### <span data-ttu-id="81700-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81700-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="81700-109">Este comando cria um Slot chamado Slot001 em um Nome de Aplicativo Web existente ContosoSite no grupo de recursos existente chamado Default-Web-WestUS no data center West US.</span><span class="sxs-lookup"><span data-stu-id="81700-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="81700-110">O comando usa um plano de Serviço de Aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="81700-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="81700-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="81700-111">PARAMETERS</span></span>

### <span data-ttu-id="81700-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="81700-112">-AppServicePlan</span></span>
<span data-ttu-id="81700-113">Nome do Plano de Serviço de Aplicativo ou ID do Plano de Serviço de Aplicativo. Se o Plano de Serviço de Slot e Aplicativo estiver em grupos de recursos diferentes, use a ID em vez do nome.</span><span class="sxs-lookup"><span data-stu-id="81700-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="81700-114">A ID do Plano de Serviço de Aplicativo pode ser recuperada usando: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id retorna a ID do Plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81700-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="81700-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="81700-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="81700-116">Configurações do aplicativo substitui hashtable</span><span class="sxs-lookup"><span data-stu-id="81700-116">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="81700-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="81700-117">-AseName</span></span>
<span data-ttu-id="81700-118">Nome do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="81700-118">App Service Environment Name</span></span>

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

### <span data-ttu-id="81700-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81700-119">-AseResourceGroupName</span></span>
<span data-ttu-id="81700-120">Nome do grupo de recursos do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="81700-120">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="81700-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81700-121">-AsJob</span></span>
<span data-ttu-id="81700-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="81700-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81700-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="81700-123">-ContainerImageName</span></span>
<span data-ttu-id="81700-124">Nome da imagem do contêiner e marca opcional, por exemplo (image:tag)</span><span class="sxs-lookup"><span data-stu-id="81700-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81700-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="81700-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="81700-126">Senha do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="81700-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81700-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="81700-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="81700-128">Url do Servidor de Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="81700-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81700-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="81700-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="81700-130">Nome de usuário do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="81700-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81700-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81700-131">-DefaultProfile</span></span>
<span data-ttu-id="81700-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="81700-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81700-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="81700-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="81700-134">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="81700-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="81700-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="81700-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="81700-136">Ignorar a opção HostNames Personalizados</span><span class="sxs-lookup"><span data-stu-id="81700-136">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="81700-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="81700-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="81700-138">Ignorar a opção de controle de origem</span><span class="sxs-lookup"><span data-stu-id="81700-138">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="81700-139">-Name</span><span class="sxs-lookup"><span data-stu-id="81700-139">-Name</span></span>
<span data-ttu-id="81700-140">Nome do Webapp</span><span class="sxs-lookup"><span data-stu-id="81700-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81700-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81700-141">-ResourceGroupName</span></span>
<span data-ttu-id="81700-142">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="81700-142">Resource Group Name</span></span>

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

### <span data-ttu-id="81700-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="81700-143">-Slot</span></span>
<span data-ttu-id="81700-144">Nome do slot do Webapp</span><span class="sxs-lookup"><span data-stu-id="81700-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81700-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="81700-145">-SourceWebApp</span></span>
<span data-ttu-id="81700-146">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="81700-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81700-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81700-147">CommonParameters</span></span>
<span data-ttu-id="81700-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81700-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81700-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81700-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81700-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81700-150">INPUTS</span></span>

### <span data-ttu-id="81700-151">System.String</span><span class="sxs-lookup"><span data-stu-id="81700-151">System.String</span></span>

### <span data-ttu-id="81700-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="81700-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="81700-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="81700-153">OUTPUTS</span></span>

### <span data-ttu-id="81700-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="81700-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="81700-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="81700-155">NOTES</span></span>

## <span data-ttu-id="81700-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81700-156">RELATED LINKS</span></span>

[<span data-ttu-id="81700-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81700-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="81700-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81700-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="81700-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81700-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="81700-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81700-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="81700-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81700-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="81700-162">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81700-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="81700-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="81700-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="81700-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="81700-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
