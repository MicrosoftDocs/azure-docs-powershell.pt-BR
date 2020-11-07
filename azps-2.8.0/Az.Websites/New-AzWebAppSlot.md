---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 6ca4eeba17af918ec73f0fe108b4179ea6513e2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774432"
---
# <span data-ttu-id="64bf4-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64bf4-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="64bf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="64bf4-103">Cria um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="64bf4-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="64bf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64bf4-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64bf4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="64bf4-106">O cmdlet **New-AzWebAppSlot** cria um slot do aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="64bf4-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="64bf4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="64bf4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64bf4-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="64bf4-109">Esse comando cria um slot chamado Slot001 em um aplicativo Web existente nomes ContosoSite no grupo de recursos existente chamado padrão-Web-Oesteus no centro de dados oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="64bf4-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="64bf4-110">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="64bf4-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="64bf4-111">OS</span><span class="sxs-lookup"><span data-stu-id="64bf4-111">PARAMETERS</span></span>

### <span data-ttu-id="64bf4-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="64bf4-112">-AppServicePlan</span></span>
<span data-ttu-id="64bf4-113">Nome do plano do serviço de aplicativo ou ID do plano do serviço de aplicativo. Se o plano do serviço de aplicativo e o slot estiverem em grupos de recursos diferentes, use a ID em vez do nome.</span><span class="sxs-lookup"><span data-stu-id="64bf4-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="64bf4-114">A ID do plano do serviço de aplicativo pode ser recuperada usando: $asp = Get-AzAppServicePlan-myRG-nome do plano de-Name myWebApp $asp. ID retorna a ID do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="64bf4-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="64bf4-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="64bf4-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="64bf4-116">Configurações do aplicativo substitui Hashtable</span><span class="sxs-lookup"><span data-stu-id="64bf4-116">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="64bf4-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="64bf4-117">-AseName</span></span>
<span data-ttu-id="64bf4-118">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="64bf4-118">App Service Environment Name</span></span>

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

### <span data-ttu-id="64bf4-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64bf4-119">-AseResourceGroupName</span></span>
<span data-ttu-id="64bf4-120">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="64bf4-120">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="64bf4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64bf4-121">-AsJob</span></span>
<span data-ttu-id="64bf4-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="64bf4-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64bf4-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="64bf4-123">-ContainerImageName</span></span>
<span data-ttu-id="64bf4-124">Nome da imagem do contêiner e marca opcional, por exemplo (imagem: marca)</span><span class="sxs-lookup"><span data-stu-id="64bf4-124">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="64bf4-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="64bf4-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="64bf4-126">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="64bf4-126">Private Container Registry Password</span></span>

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

### <span data-ttu-id="64bf4-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="64bf4-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="64bf4-128">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="64bf4-128">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="64bf4-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="64bf4-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="64bf4-130">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="64bf4-130">Private Container Registry Username</span></span>

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

### <span data-ttu-id="64bf4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bf4-131">-DefaultProfile</span></span>
<span data-ttu-id="64bf4-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64bf4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64bf4-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="64bf4-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="64bf4-134">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="64bf4-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="64bf4-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="64bf4-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="64bf4-136">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="64bf4-136">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="64bf4-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="64bf4-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="64bf4-138">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="64bf4-138">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="64bf4-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="64bf4-139">-Name</span></span>
<span data-ttu-id="64bf4-140">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="64bf4-140">Webapp Name</span></span>

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

### <span data-ttu-id="64bf4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64bf4-141">-ResourceGroupName</span></span>
<span data-ttu-id="64bf4-142">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="64bf4-142">Resource Group Name</span></span>

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

### <span data-ttu-id="64bf4-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="64bf4-143">-Slot</span></span>
<span data-ttu-id="64bf4-144">Nome do slot do webapp</span><span class="sxs-lookup"><span data-stu-id="64bf4-144">Webapp Slot Name</span></span>

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

### <span data-ttu-id="64bf4-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="64bf4-145">-SourceWebApp</span></span>
<span data-ttu-id="64bf4-146">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="64bf4-146">Source WebApp Object</span></span>

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

### <span data-ttu-id="64bf4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bf4-147">CommonParameters</span></span>
<span data-ttu-id="64bf4-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bf4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bf4-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64bf4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bf4-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64bf4-150">INPUTS</span></span>

### <span data-ttu-id="64bf4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="64bf4-151">System.String</span></span>

### <span data-ttu-id="64bf4-152">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="64bf4-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="64bf4-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64bf4-153">OUTPUTS</span></span>

### <span data-ttu-id="64bf4-154">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="64bf4-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="64bf4-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64bf4-155">NOTES</span></span>

## <span data-ttu-id="64bf4-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64bf4-156">RELATED LINKS</span></span>

[<span data-ttu-id="64bf4-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64bf4-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="64bf4-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64bf4-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="64bf4-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64bf4-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="64bf4-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64bf4-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="64bf4-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64bf4-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="64bf4-162">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64bf4-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="64bf4-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="64bf4-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="64bf4-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="64bf4-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)