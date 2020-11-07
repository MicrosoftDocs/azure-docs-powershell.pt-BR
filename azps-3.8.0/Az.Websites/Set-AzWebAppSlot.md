---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942601"
---
# <span data-ttu-id="d8436-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d8436-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="d8436-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8436-102">SYNOPSIS</span></span>
<span data-ttu-id="d8436-103">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d8436-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="d8436-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8436-104">SYNTAX</span></span>

### <span data-ttu-id="d8436-105">Eles</span><span class="sxs-lookup"><span data-stu-id="d8436-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8436-106">S2</span><span class="sxs-lookup"><span data-stu-id="d8436-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8436-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8436-107">DESCRIPTION</span></span>
<span data-ttu-id="d8436-108">O cmdlet **set-AzWebApp** define um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d8436-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="d8436-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8436-109">EXAMPLES</span></span>

### <span data-ttu-id="d8436-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8436-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="d8436-111">Esse comando altera o plano appservice associado ao Slot001, no WebApp ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="d8436-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d8436-112">Use o link para saber mais sobre como alterar o plano appservice e restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="d8436-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="d8436-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="d8436-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="d8436-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d8436-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="d8436-115">Esse comando define HttpLoggingEnabled como true para o slot Slot001 pertencentes ao ContosoWebApp do aplicativo Web associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="d8436-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d8436-116">OS</span><span class="sxs-lookup"><span data-stu-id="d8436-116">PARAMETERS</span></span>

### <span data-ttu-id="d8436-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="d8436-117">-AlwaysOn</span></span>
<span data-ttu-id="d8436-118">Assegure-se de que o aplicativo Web seja carregado o tempo todo, em vez de não ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="d8436-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8436-119">-AppServicePlan</span></span>
<span data-ttu-id="d8436-120">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d8436-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="d8436-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="d8436-121">-AppSettings</span></span>
<span data-ttu-id="d8436-122">HashTable das configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8436-122">App Settings HashTable.</span></span> <span data-ttu-id="d8436-123">As configurações do aplicativo existente serão substituídas, removendo as configurações não fornecidas.</span><span class="sxs-lookup"><span data-stu-id="d8436-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8436-124">-AsJob</span></span>
<span data-ttu-id="d8436-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d8436-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8436-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d8436-126">-AssignIdentity</span></span>
<span data-ttu-id="d8436-127">Habilitar/desabilitar o MSI em um slot existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="d8436-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="d8436-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="d8436-129">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="d8436-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="d8436-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="d8436-130">-AzureStoragePath</span></span>
<span data-ttu-id="d8436-131">Armazenamento do Azure para montagem dentro de um aplicativo Web para contêiner.</span><span class="sxs-lookup"><span data-stu-id="d8436-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="d8436-132">Usar o New-AzureRmWebAppAzureStoragePath para criá-lo</span><span class="sxs-lookup"><span data-stu-id="d8436-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="d8436-133">-ConnectionStrings</span></span>
<span data-ttu-id="d8436-134">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="d8436-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="d8436-135">-ContainerImageName</span></span>
<span data-ttu-id="d8436-136">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="d8436-136">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="d8436-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="d8436-138">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="d8436-138">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="d8436-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="d8436-140">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="d8436-140">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="d8436-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="d8436-142">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="d8436-142">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-143">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="d8436-143">-DefaultDocuments</span></span>
<span data-ttu-id="d8436-144">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="d8436-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8436-145">-DefaultProfile</span></span>
<span data-ttu-id="d8436-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8436-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8436-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d8436-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="d8436-148">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="d8436-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="d8436-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="d8436-150">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="d8436-150">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-151">-Ftpsstate</span><span class="sxs-lookup"><span data-stu-id="d8436-151">-FtpsState</span></span>
<span data-ttu-id="d8436-152">Defina o valor do estado de FTPS para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8436-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="d8436-153">Valores permitidos [permitidos | Desativado | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="d8436-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="d8436-154">-HandlerMappings</span></span>
<span data-ttu-id="d8436-155">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="d8436-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d8436-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="d8436-157">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="d8436-157">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d8436-158">-HttpsOnly</span></span>
<span data-ttu-id="d8436-159">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um slot existente</span><span class="sxs-lookup"><span data-stu-id="d8436-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="d8436-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="d8436-161">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="d8436-161">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d8436-162">-MinTlsVersion</span></span>
<span data-ttu-id="d8436-163">A versão mínima do TLS necessária para solicitações SSL.</span><span class="sxs-lookup"><span data-stu-id="d8436-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="d8436-164">Valores permitidos [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="d8436-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8436-165">-Name</span></span>
<span data-ttu-id="d8436-166">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="d8436-166">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="d8436-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="d8436-168">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d8436-168">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="d8436-169">-NumberOfWorkers</span></span>
<span data-ttu-id="d8436-170">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="d8436-170">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="d8436-171">-PhpVersion</span></span>
<span data-ttu-id="d8436-172">Versão do php</span><span class="sxs-lookup"><span data-stu-id="d8436-172">Php Version</span></span>

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

### <span data-ttu-id="d8436-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="d8436-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="d8436-174">Booleano de rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="d8436-174">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8436-175">-ResourceGroupName</span></span>
<span data-ttu-id="d8436-176">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d8436-176">Resource Group Name</span></span>

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

### <span data-ttu-id="d8436-177">-Slot</span><span class="sxs-lookup"><span data-stu-id="d8436-177">-Slot</span></span>
<span data-ttu-id="d8436-178">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="d8436-178">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="d8436-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="d8436-180">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d8436-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d8436-181">-WebApp</span></span>
<span data-ttu-id="d8436-182">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="d8436-182">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d8436-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="d8436-184">Booleano habilitados para Web Sockets</span><span class="sxs-lookup"><span data-stu-id="d8436-184">Web Sockets Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8436-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8436-185">CommonParameters</span></span>
<span data-ttu-id="d8436-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8436-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8436-187">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8436-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8436-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8436-188">INPUTS</span></span>

### <span data-ttu-id="d8436-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d8436-189">System.Int32</span></span>

### <span data-ttu-id="d8436-190">System. String</span><span class="sxs-lookup"><span data-stu-id="d8436-190">System.String</span></span>

### <span data-ttu-id="d8436-191">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d8436-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d8436-192">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8436-192">OUTPUTS</span></span>

### <span data-ttu-id="d8436-193">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d8436-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d8436-194">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8436-194">NOTES</span></span>

## <span data-ttu-id="d8436-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8436-195">RELATED LINKS</span></span>

[<span data-ttu-id="d8436-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d8436-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d8436-197">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d8436-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d8436-198">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d8436-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d8436-199">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d8436-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="d8436-200">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d8436-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d8436-201">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d8436-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d8436-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d8436-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
