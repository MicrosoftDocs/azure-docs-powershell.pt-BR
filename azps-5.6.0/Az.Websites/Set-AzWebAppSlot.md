---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d07d85aa9747982f223d45c40fc8897a0b0e3e73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893040"
---
# <span data-ttu-id="8a0d2-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8a0d2-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="8a0d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0d2-103">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="8a0d2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8a0d2-104">SYNTAX</span></span>

### <span data-ttu-id="8a0d2-105">S1</span><span class="sxs-lookup"><span data-stu-id="8a0d2-105">S1</span></span>
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

### <span data-ttu-id="8a0d2-106">S2</span><span class="sxs-lookup"><span data-stu-id="8a0d2-106">S2</span></span>
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

## <span data-ttu-id="8a0d2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8a0d2-107">DESCRIPTION</span></span>
<span data-ttu-id="8a0d2-108">O cmdlet **Set-AzWebApp** define um Slot do Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="8a0d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a0d2-109">EXAMPLES</span></span>

### <span data-ttu-id="8a0d2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8a0d2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="8a0d2-111">Este comando altera o plano de appservice associado ao Slot001, no Webapp ContosoWebApp associado ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="8a0d2-112">Use o link para saber mais sobre como alterar o plano de appservice e as restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="8a0d2-113"> https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="8a0d2-113">https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="8a0d2-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8a0d2-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="8a0d2-115">Este comando define HttpLoggingEnabled como true para Slot Slot001 pertencente ao Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="8a0d2-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="8a0d2-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8a0d2-116">Example 3</span></span>

<span data-ttu-id="8a0d2-117">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="8a0d2-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="8a0d2-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="8a0d2-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8a0d2-119">PARAMETERS</span></span>

### <span data-ttu-id="8a0d2-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="8a0d2-120">-AlwaysOn</span></span>
<span data-ttu-id="8a0d2-121">Verifique se o aplicativo Web é carregado o tempo todo, em vez de descarregado após ficar ocioso.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="8a0d2-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8a0d2-122">-AppServicePlan</span></span>
<span data-ttu-id="8a0d2-123">Nome do Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="8a0d2-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="8a0d2-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="8a0d2-124">-AppSettings</span></span>
<span data-ttu-id="8a0d2-125">HashTable de Configurações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-125">App Settings HashTable.</span></span> <span data-ttu-id="8a0d2-126">As configurações de aplicativo existentes serão substituídas, removendo todas as configurações que não são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="8a0d2-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a0d2-127">-AsJob</span></span>
<span data-ttu-id="8a0d2-128">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8a0d2-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a0d2-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8a0d2-129">-AssignIdentity</span></span>
<span data-ttu-id="8a0d2-130">Habilitar/desabilitar o MSI em um slot existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="8a0d2-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="8a0d2-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="8a0d2-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="8a0d2-132">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="8a0d2-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="8a0d2-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="8a0d2-133">-AzureStoragePath</span></span>
<span data-ttu-id="8a0d2-134">Armazenamento do Azure para montar dentro de um Aplicativo Web para Contêiner.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="8a0d2-135">Usar New-AzureRmWebAppAzureStoragePath para criar</span><span class="sxs-lookup"><span data-stu-id="8a0d2-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="8a0d2-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="8a0d2-136">-ConnectionStrings</span></span>
<span data-ttu-id="8a0d2-137">HashTable de Cadeias de Caracteres de Conexão</span><span class="sxs-lookup"><span data-stu-id="8a0d2-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="8a0d2-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="8a0d2-138">-ContainerImageName</span></span>
<span data-ttu-id="8a0d2-139">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="8a0d2-139">Container Image Name</span></span>

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

### <span data-ttu-id="8a0d2-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="8a0d2-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="8a0d2-141">Senha do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="8a0d2-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="8a0d2-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="8a0d2-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="8a0d2-143">Url do Servidor de Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="8a0d2-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="8a0d2-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="8a0d2-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="8a0d2-145">Nome de usuário do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="8a0d2-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="8a0d2-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="8a0d2-146">-DefaultDocuments</span></span>
<span data-ttu-id="8a0d2-147">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="8a0d2-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="8a0d2-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0d2-148">-DefaultProfile</span></span>
<span data-ttu-id="8a0d2-149">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a0d2-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8a0d2-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="8a0d2-151">Boolean habilitado para log de erro detalhado</span><span class="sxs-lookup"><span data-stu-id="8a0d2-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="8a0d2-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="8a0d2-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="8a0d2-153">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="8a0d2-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="8a0d2-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="8a0d2-154">-FtpsState</span></span>
<span data-ttu-id="8a0d2-155">De definir o valor de estado Ftps para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="8a0d2-156">Valores permitidos [AllAllowed | Desabilitado | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="8a0d2-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="8a0d2-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="8a0d2-157">-HandlerMappings</span></span>
<span data-ttu-id="8a0d2-158">IList de Mapeamentos de Manipuladores</span><span class="sxs-lookup"><span data-stu-id="8a0d2-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="8a0d2-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8a0d2-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="8a0d2-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="8a0d2-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="8a0d2-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8a0d2-161">-HttpsOnly</span></span>
<span data-ttu-id="8a0d2-162">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um slot existente</span><span class="sxs-lookup"><span data-stu-id="8a0d2-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="8a0d2-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="8a0d2-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="8a0d2-164">Nome do modo pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="8a0d2-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="8a0d2-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8a0d2-165">-MinTlsVersion</span></span>
<span data-ttu-id="8a0d2-166">A versão mínima do TLS necessária para solicitações SSL.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="8a0d2-167">Valores permitidos [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="8a0d2-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="8a0d2-168">-Name</span><span class="sxs-lookup"><span data-stu-id="8a0d2-168">-Name</span></span>
<span data-ttu-id="8a0d2-169">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="8a0d2-169">WebApp Name</span></span>

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

### <span data-ttu-id="8a0d2-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="8a0d2-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="8a0d2-171">Versão do Net Framework</span><span class="sxs-lookup"><span data-stu-id="8a0d2-171">Net Framework Version</span></span>

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

### <span data-ttu-id="8a0d2-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="8a0d2-172">-NumberOfWorkers</span></span>
<span data-ttu-id="8a0d2-173">O número de funcionários a serem alocados</span><span class="sxs-lookup"><span data-stu-id="8a0d2-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="8a0d2-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="8a0d2-174">-PhpVersion</span></span>
<span data-ttu-id="8a0d2-175">Versão Php</span><span class="sxs-lookup"><span data-stu-id="8a0d2-175">Php Version</span></span>

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

### <span data-ttu-id="8a0d2-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="8a0d2-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="8a0d2-177">Boolean habilitado para rastreamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="8a0d2-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="8a0d2-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0d2-178">-ResourceGroupName</span></span>
<span data-ttu-id="8a0d2-179">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8a0d2-179">Resource Group Name</span></span>

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

### <span data-ttu-id="8a0d2-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="8a0d2-180">-Slot</span></span>
<span data-ttu-id="8a0d2-181">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="8a0d2-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8a0d2-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="8a0d2-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="8a0d2-183">Usar booleano de processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="8a0d2-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="8a0d2-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8a0d2-184">-WebApp</span></span>
<span data-ttu-id="8a0d2-185">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="8a0d2-185">WebApp Object</span></span>

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

### <span data-ttu-id="8a0d2-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="8a0d2-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="8a0d2-187">Boolean habilitado para soquetes web</span><span class="sxs-lookup"><span data-stu-id="8a0d2-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="8a0d2-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0d2-188">CommonParameters</span></span>
<span data-ttu-id="8a0d2-189">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a0d2-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0d2-190">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a0d2-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0d2-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a0d2-191">INPUTS</span></span>

### <span data-ttu-id="8a0d2-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8a0d2-192">System.Int32</span></span>

### <span data-ttu-id="8a0d2-193">System.String</span><span class="sxs-lookup"><span data-stu-id="8a0d2-193">System.String</span></span>

### <span data-ttu-id="8a0d2-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8a0d2-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8a0d2-195">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8a0d2-195">OUTPUTS</span></span>

### <span data-ttu-id="8a0d2-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8a0d2-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8a0d2-197">NOTES</span><span class="sxs-lookup"><span data-stu-id="8a0d2-197">NOTES</span></span>

## <span data-ttu-id="8a0d2-198">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a0d2-198">RELATED LINKS</span></span>

[<span data-ttu-id="8a0d2-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8a0d2-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8a0d2-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8a0d2-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8a0d2-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8a0d2-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8a0d2-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8a0d2-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8a0d2-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8a0d2-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8a0d2-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8a0d2-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8a0d2-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8a0d2-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
