---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439978"
---
# <span data-ttu-id="77ebb-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77ebb-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="77ebb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="77ebb-103">Cria um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="77ebb-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77ebb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77ebb-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77ebb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77ebb-105">DESCRIPTION</span></span>
<span data-ttu-id="77ebb-106">O cmdlet **New-AzureRmWebAppSlot** cria um slot do aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="77ebb-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="77ebb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77ebb-107">EXAMPLES</span></span>

### <span data-ttu-id="77ebb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77ebb-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="77ebb-109">Esse comando cria um slot chamado Slot001 em um aplicativo Web existente nomes ContosoSite no grupo de recursos existente chamado padrão-Web-Oesteus no centro de dados oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="77ebb-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="77ebb-110">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="77ebb-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="77ebb-111">OS</span><span class="sxs-lookup"><span data-stu-id="77ebb-111">PARAMETERS</span></span>

### <span data-ttu-id="77ebb-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="77ebb-112">-AppServicePlan</span></span>
<span data-ttu-id="77ebb-113">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="77ebb-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="77ebb-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="77ebb-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="77ebb-115">Configurações do aplicativo substitui Hashtable</span><span class="sxs-lookup"><span data-stu-id="77ebb-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="77ebb-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="77ebb-116">-AseName</span></span>
<span data-ttu-id="77ebb-117">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="77ebb-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="77ebb-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ebb-118">-AseResourceGroupName</span></span>
<span data-ttu-id="77ebb-119">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="77ebb-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="77ebb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77ebb-120">-AsJob</span></span>
<span data-ttu-id="77ebb-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="77ebb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77ebb-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="77ebb-122">-ContainerImageName</span></span>
<span data-ttu-id="77ebb-123">Nome da imagem do contêiner e marca opcional, por exemplo (imagem: marca)</span><span class="sxs-lookup"><span data-stu-id="77ebb-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="77ebb-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="77ebb-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="77ebb-125">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="77ebb-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="77ebb-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="77ebb-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="77ebb-127">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="77ebb-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="77ebb-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="77ebb-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="77ebb-129">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="77ebb-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="77ebb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ebb-130">-DefaultProfile</span></span>
<span data-ttu-id="77ebb-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77ebb-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77ebb-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="77ebb-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="77ebb-133">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="77ebb-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="77ebb-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="77ebb-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="77ebb-135">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="77ebb-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="77ebb-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="77ebb-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="77ebb-137">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="77ebb-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="77ebb-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="77ebb-138">-Name</span></span>
<span data-ttu-id="77ebb-139">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="77ebb-139">Webapp Name</span></span>

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

### <span data-ttu-id="77ebb-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ebb-140">-ResourceGroupName</span></span>
<span data-ttu-id="77ebb-141">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="77ebb-141">Resource Group Name</span></span>

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

### <span data-ttu-id="77ebb-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="77ebb-142">-Slot</span></span>
<span data-ttu-id="77ebb-143">Nome do slot do webapp</span><span class="sxs-lookup"><span data-stu-id="77ebb-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="77ebb-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="77ebb-144">-SourceWebApp</span></span>
<span data-ttu-id="77ebb-145">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="77ebb-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="77ebb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ebb-146">CommonParameters</span></span>
<span data-ttu-id="77ebb-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77ebb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ebb-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ebb-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ebb-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77ebb-149">INPUTS</span></span>

### <span data-ttu-id="77ebb-150">System. String</span><span class="sxs-lookup"><span data-stu-id="77ebb-150">System.String</span></span>

### <span data-ttu-id="77ebb-151">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="77ebb-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="77ebb-152">Parâmetros: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77ebb-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="77ebb-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77ebb-153">OUTPUTS</span></span>

### <span data-ttu-id="77ebb-154">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="77ebb-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="77ebb-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77ebb-155">NOTES</span></span>

## <span data-ttu-id="77ebb-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77ebb-156">RELATED LINKS</span></span>

[<span data-ttu-id="77ebb-157">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77ebb-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="77ebb-158">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77ebb-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="77ebb-159">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77ebb-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="77ebb-160">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77ebb-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="77ebb-161">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77ebb-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="77ebb-162">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77ebb-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="77ebb-163">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="77ebb-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="77ebb-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="77ebb-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
