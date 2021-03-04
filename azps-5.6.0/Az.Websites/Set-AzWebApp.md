---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2f79abc7e5d6961c5e3f09deb843490d78c4614f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893041"
---
# <span data-ttu-id="42b86-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-101">Set-AzWebApp</span></span>

## <span data-ttu-id="42b86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42b86-102">SYNOPSIS</span></span>
<span data-ttu-id="42b86-103">Modifica um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="42b86-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="42b86-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="42b86-104">SYNTAX</span></span>

### <span data-ttu-id="42b86-105">S1</span><span class="sxs-lookup"><span data-stu-id="42b86-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42b86-106">S2</span><span class="sxs-lookup"><span data-stu-id="42b86-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42b86-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="42b86-107">DESCRIPTION</span></span>
<span data-ttu-id="42b86-108">O cmdlet **Set-AzWebApp** define um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="42b86-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="42b86-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42b86-109">EXAMPLES</span></span>

### <span data-ttu-id="42b86-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42b86-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="42b86-111">Este comando altera o plano de appservice associado ao Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="42b86-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="42b86-112">Use o link para saber mais sobre como alterar o plano de appservice e as restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="42b86-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="42b86-113"> https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="42b86-113">https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="42b86-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="42b86-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="42b86-115">Este comando define HttpLoggingEnabled como true para Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="42b86-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="42b86-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="42b86-116">Example 3</span></span>

<span data-ttu-id="42b86-117">Modifica um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="42b86-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="42b86-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="42b86-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="42b86-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="42b86-119">Example 4</span></span>

<span data-ttu-id="42b86-120">O exemplo a seguir cria uma cadeia de conexão chamada myConnectionString para Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="42b86-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="42b86-121">Isso substitui todas as cadeias de conexão existentes para Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="42b86-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="42b86-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="42b86-122">PARAMETERS</span></span>

### <span data-ttu-id="42b86-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="42b86-123">-AlwaysOn</span></span>
<span data-ttu-id="42b86-124">Verifique se o aplicativo Web é carregado o tempo todo, em vez de descarregado após ficar ocioso.</span><span class="sxs-lookup"><span data-stu-id="42b86-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="42b86-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="42b86-125">-AppServicePlan</span></span>
<span data-ttu-id="42b86-126">Nome do Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="42b86-126">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="42b86-127">-AppSettings</span></span>
<span data-ttu-id="42b86-128">HashTable de Configurações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b86-128">App Settings HashTable.</span></span> <span data-ttu-id="42b86-129">As configurações de aplicativo existentes serão substituídas, removendo todas as configurações que não são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="42b86-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42b86-130">-AsJob</span></span>
<span data-ttu-id="42b86-131">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="42b86-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42b86-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="42b86-132">-AssignIdentity</span></span>
<span data-ttu-id="42b86-133">Habilitar/desabilitar o MSI em um webapp ou functionapp do azure existente</span><span class="sxs-lookup"><span data-stu-id="42b86-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="42b86-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="42b86-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="42b86-135">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="42b86-135">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="42b86-136">-AzureStoragePath</span></span>
<span data-ttu-id="42b86-137">Armazenamento do Azure para montar dentro de um Aplicativo Web para Contêiner.</span><span class="sxs-lookup"><span data-stu-id="42b86-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="42b86-138">Usar New-AzureRmWebAppAzureStoragePath para criar</span><span class="sxs-lookup"><span data-stu-id="42b86-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="42b86-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="42b86-139">-ConnectionStrings</span></span>
<span data-ttu-id="42b86-140">HashTable de Cadeias de Caracteres de Conexão</span><span class="sxs-lookup"><span data-stu-id="42b86-140">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="42b86-141">-ContainerImageName</span></span>
<span data-ttu-id="42b86-142">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="42b86-142">Container Image Name</span></span>

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

### <span data-ttu-id="42b86-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="42b86-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="42b86-144">Senha do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="42b86-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="42b86-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="42b86-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="42b86-146">Url do Servidor de Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="42b86-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="42b86-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="42b86-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="42b86-148">Nome de usuário do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="42b86-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="42b86-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="42b86-149">-DefaultDocuments</span></span>
<span data-ttu-id="42b86-150">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="42b86-150">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b86-151">-DefaultProfile</span></span>
<span data-ttu-id="42b86-152">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="42b86-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42b86-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="42b86-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="42b86-154">Boolean habilitado para log de erro detalhado</span><span class="sxs-lookup"><span data-stu-id="42b86-154">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="42b86-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="42b86-156">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="42b86-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="42b86-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="42b86-157">-FtpsState</span></span>
<span data-ttu-id="42b86-158">De definir o valor de estado Ftps para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b86-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="42b86-159">Valores permitidos [AllAllowed | Desabilitado | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="42b86-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="42b86-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="42b86-160">-HandlerMappings</span></span>
<span data-ttu-id="42b86-161">IList de Mapeamentos de Manipuladores</span><span class="sxs-lookup"><span data-stu-id="42b86-161">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="42b86-162">-HostNames</span></span>
<span data-ttu-id="42b86-163">Matriz de cadeias de caracteres HostNames do WebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-163">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="42b86-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="42b86-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="42b86-165">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="42b86-166">-HttpsOnly</span></span>
<span data-ttu-id="42b86-167">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um webapp ou functionapp do azure existente</span><span class="sxs-lookup"><span data-stu-id="42b86-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="42b86-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="42b86-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="42b86-169">Nome do modo pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="42b86-169">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="42b86-170">-MinTlsVersion</span></span>
<span data-ttu-id="42b86-171">A versão mínima do TLS necessária para solicitações SSL.</span><span class="sxs-lookup"><span data-stu-id="42b86-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="42b86-172">Valores permitidos [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="42b86-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="42b86-173">-Name</span><span class="sxs-lookup"><span data-stu-id="42b86-173">-Name</span></span>
<span data-ttu-id="42b86-174">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-174">WebApp Name</span></span>

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

### <span data-ttu-id="42b86-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="42b86-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="42b86-176">Versão do Net Framework</span><span class="sxs-lookup"><span data-stu-id="42b86-176">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="42b86-177">-NumberOfWorkers</span></span>
<span data-ttu-id="42b86-178">O número de funcionários a serem alocados</span><span class="sxs-lookup"><span data-stu-id="42b86-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="42b86-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="42b86-179">-PhpVersion</span></span>
<span data-ttu-id="42b86-180">Versão Php</span><span class="sxs-lookup"><span data-stu-id="42b86-180">Php Version</span></span>

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

### <span data-ttu-id="42b86-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="42b86-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="42b86-182">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="42b86-182">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b86-183">-ResourceGroupName</span></span>
<span data-ttu-id="42b86-184">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="42b86-184">Resource Group Name</span></span>

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

### <span data-ttu-id="42b86-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="42b86-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="42b86-186">Usar booleano de processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="42b86-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="42b86-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-187">-WebApp</span></span>
<span data-ttu-id="42b86-188">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-188">WebApp Object</span></span>

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

### <span data-ttu-id="42b86-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="42b86-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="42b86-190">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="42b86-190">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b86-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b86-191">CommonParameters</span></span>
<span data-ttu-id="42b86-192">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b86-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b86-193">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42b86-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b86-194">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42b86-194">INPUTS</span></span>

### <span data-ttu-id="42b86-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="42b86-195">System.Int32</span></span>

### <span data-ttu-id="42b86-196">System.String</span><span class="sxs-lookup"><span data-stu-id="42b86-196">System.String</span></span>

### <span data-ttu-id="42b86-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="42b86-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="42b86-198">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="42b86-198">OUTPUTS</span></span>

### <span data-ttu-id="42b86-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="42b86-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="42b86-200">NOTES</span><span class="sxs-lookup"><span data-stu-id="42b86-200">NOTES</span></span>
<span data-ttu-id="42b86-201">Abaixo o cmdlet fornecido ajudará você a atualizar o Azure Web App para **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="42b86-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="42b86-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadados" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="42b86-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="42b86-203">Substitua os valores de Default-Web-WestUS pelo nome do grupo de recursos do webapp e contosoWebApp pelo nome do webapp.</span><span class="sxs-lookup"><span data-stu-id="42b86-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="42b86-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42b86-204">RELATED LINKS</span></span>

[<span data-ttu-id="42b86-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="42b86-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="42b86-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="42b86-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="42b86-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="42b86-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42b86-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="42b86-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="42b86-211">New-AzResource</span></span>](./New-AzResource.md)
