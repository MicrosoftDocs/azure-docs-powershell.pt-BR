---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118848"
---
# <span data-ttu-id="08ee2-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ee2-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="08ee2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="08ee2-103">Cria um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="08ee2-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="08ee2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08ee2-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08ee2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="08ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="08ee2-106">O cmdlet **New-AzWebAppSlot** cria um Slot do Azure Web App em um determinado grupo de recursos que usa o plano de Serviço de Aplicativos e o data center especificados.</span><span class="sxs-lookup"><span data-stu-id="08ee2-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="08ee2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08ee2-107">EXAMPLES</span></span>

### <span data-ttu-id="08ee2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="08ee2-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="08ee2-109">Esse comando cria um Slot chamado Slot001 sob um Web App existente chamado ContosoSite no grupo de recursos existente chamado Default-Web-WestUS no data center West US.</span><span class="sxs-lookup"><span data-stu-id="08ee2-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="08ee2-110">O comando usa um plano de Serviço de Aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="08ee2-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="08ee2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08ee2-111">PARAMETERS</span></span>

### <span data-ttu-id="08ee2-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="08ee2-112">-AppServicePlan</span></span>
<span data-ttu-id="08ee2-113">Nome do Plano de Serviço de Aplicativo ou ID do Plano de Serviço de Aplicativo. Se o Slot e o Plano de Serviço de Aplicativos estão em grupos de recursos diferentes, use a ID em vez do nome.</span><span class="sxs-lookup"><span data-stu-id="08ee2-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="08ee2-114">A ID do Plano de Serviço de Aplicativo pode ser recuperada usando: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id retorna a ID do Plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="08ee2-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="08ee2-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="08ee2-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="08ee2-116">Configurações do Aplicativo substitui a tabela hash</span><span class="sxs-lookup"><span data-stu-id="08ee2-116">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="08ee2-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="08ee2-117">-AseName</span></span>
<span data-ttu-id="08ee2-118">Nome do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="08ee2-118">App Service Environment Name</span></span>

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

### <span data-ttu-id="08ee2-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ee2-119">-AseResourceGroupName</span></span>
<span data-ttu-id="08ee2-120">Nome do grupo de recursos de ambiente de serviço de aplicativos</span><span class="sxs-lookup"><span data-stu-id="08ee2-120">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="08ee2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08ee2-121">-AsJob</span></span>
<span data-ttu-id="08ee2-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="08ee2-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08ee2-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="08ee2-123">-ContainerImageName</span></span>
<span data-ttu-id="08ee2-124">Nome da Imagem do Contêiner e marca opcional, por exemplo (imagem:marca)</span><span class="sxs-lookup"><span data-stu-id="08ee2-124">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="08ee2-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="08ee2-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="08ee2-126">Senha do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="08ee2-126">Private Container Registry Password</span></span>

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

### <span data-ttu-id="08ee2-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="08ee2-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="08ee2-128">Url do Servidor de Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="08ee2-128">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="08ee2-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="08ee2-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="08ee2-130">Nome de usuário do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="08ee2-130">Private Container Registry Username</span></span>

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

### <span data-ttu-id="08ee2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ee2-131">-DefaultProfile</span></span>
<span data-ttu-id="08ee2-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="08ee2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08ee2-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="08ee2-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="08ee2-134">Habilitar/Desabilitar contêiner de implantação contínua na Web.</span><span class="sxs-lookup"><span data-stu-id="08ee2-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="08ee2-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="08ee2-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="08ee2-136">Ignorar a opção Nomes de Host Personalizados</span><span class="sxs-lookup"><span data-stu-id="08ee2-136">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="08ee2-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="08ee2-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="08ee2-138">Ignorar Opção de Controle de Origem</span><span class="sxs-lookup"><span data-stu-id="08ee2-138">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="08ee2-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="08ee2-139">-Name</span></span>
<span data-ttu-id="08ee2-140">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="08ee2-140">Webapp Name</span></span>

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

### <span data-ttu-id="08ee2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ee2-141">-ResourceGroupName</span></span>
<span data-ttu-id="08ee2-142">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="08ee2-142">Resource Group Name</span></span>

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

### <span data-ttu-id="08ee2-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="08ee2-143">-Slot</span></span>
<span data-ttu-id="08ee2-144">Nome do slot do Webapp</span><span class="sxs-lookup"><span data-stu-id="08ee2-144">Webapp Slot Name</span></span>

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

### <span data-ttu-id="08ee2-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="08ee2-145">-SourceWebApp</span></span>
<span data-ttu-id="08ee2-146">Objeto Source WebApp</span><span class="sxs-lookup"><span data-stu-id="08ee2-146">Source WebApp Object</span></span>

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

### <span data-ttu-id="08ee2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ee2-147">CommonParameters</span></span>
<span data-ttu-id="08ee2-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ee2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ee2-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ee2-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ee2-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="08ee2-150">INPUTS</span></span>

### <span data-ttu-id="08ee2-151">System.String</span><span class="sxs-lookup"><span data-stu-id="08ee2-151">System.String</span></span>

### <span data-ttu-id="08ee2-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="08ee2-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08ee2-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="08ee2-153">OUTPUTS</span></span>

### <span data-ttu-id="08ee2-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="08ee2-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08ee2-155">Notas</span><span class="sxs-lookup"><span data-stu-id="08ee2-155">NOTES</span></span>

## <span data-ttu-id="08ee2-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08ee2-156">RELATED LINKS</span></span>

[<span data-ttu-id="08ee2-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ee2-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="08ee2-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ee2-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="08ee2-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ee2-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="08ee2-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ee2-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="08ee2-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ee2-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="08ee2-162">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ee2-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="08ee2-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="08ee2-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="08ee2-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="08ee2-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
