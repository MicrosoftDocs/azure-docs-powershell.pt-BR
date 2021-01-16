---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259045"
---
# <span data-ttu-id="69c91-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-101">Set-AzWebApp</span></span>

## <span data-ttu-id="69c91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69c91-102">SYNOPSIS</span></span>
<span data-ttu-id="69c91-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="69c91-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="69c91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69c91-104">SYNTAX</span></span>

### <span data-ttu-id="69c91-105">Eles</span><span class="sxs-lookup"><span data-stu-id="69c91-105">S1</span></span>
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

### <span data-ttu-id="69c91-106">S2</span><span class="sxs-lookup"><span data-stu-id="69c91-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c91-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69c91-107">DESCRIPTION</span></span>
<span data-ttu-id="69c91-108">O cmdlet **set-AzWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="69c91-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="69c91-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69c91-109">EXAMPLES</span></span>

### <span data-ttu-id="69c91-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69c91-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="69c91-111">Esse comando altera o plano appservice associado ao aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="69c91-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="69c91-112">Use o link para saber mais sobre como alterar o plano appservice e restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="69c91-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="69c91-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="69c91-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="69c91-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="69c91-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="69c91-115">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="69c91-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="69c91-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="69c91-116">Example 3</span></span>

<span data-ttu-id="69c91-117">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="69c91-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="69c91-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="69c91-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="69c91-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="69c91-119">Example 4</span></span>

<span data-ttu-id="69c91-120">O exemplo a seguir cria uma cadeia de conexão chamada myconnectstring para Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="69c91-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="69c91-121">Isso substitui todas as cadeias de conexão existentes para o aplicativo Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="69c91-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="69c91-122">OS</span><span class="sxs-lookup"><span data-stu-id="69c91-122">PARAMETERS</span></span>

### <span data-ttu-id="69c91-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="69c91-123">-AlwaysOn</span></span>
<span data-ttu-id="69c91-124">Assegure-se de que o aplicativo Web seja carregado o tempo todo, em vez de não ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="69c91-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="69c91-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69c91-125">-AppServicePlan</span></span>
<span data-ttu-id="69c91-126">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="69c91-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="69c91-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="69c91-127">-AppSettings</span></span>
<span data-ttu-id="69c91-128">HashTable das configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69c91-128">App Settings HashTable.</span></span> <span data-ttu-id="69c91-129">As configurações do aplicativo existente serão substituídas, removendo as configurações não fornecidas.</span><span class="sxs-lookup"><span data-stu-id="69c91-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="69c91-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69c91-130">-AsJob</span></span>
<span data-ttu-id="69c91-131">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="69c91-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69c91-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="69c91-132">-AssignIdentity</span></span>
<span data-ttu-id="69c91-133">Habilitar/desabilitar o MSI em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="69c91-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="69c91-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="69c91-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="69c91-135">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="69c91-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="69c91-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="69c91-136">-AzureStoragePath</span></span>
<span data-ttu-id="69c91-137">Armazenamento do Azure para montagem dentro de um aplicativo Web para contêiner.</span><span class="sxs-lookup"><span data-stu-id="69c91-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="69c91-138">Usar o New-AzureRmWebAppAzureStoragePath para criá-lo</span><span class="sxs-lookup"><span data-stu-id="69c91-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="69c91-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="69c91-139">-ConnectionStrings</span></span>
<span data-ttu-id="69c91-140">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="69c91-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="69c91-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="69c91-141">-ContainerImageName</span></span>
<span data-ttu-id="69c91-142">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="69c91-142">Container Image Name</span></span>

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

### <span data-ttu-id="69c91-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="69c91-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="69c91-144">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="69c91-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="69c91-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="69c91-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="69c91-146">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="69c91-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="69c91-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="69c91-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="69c91-148">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="69c91-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="69c91-149">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="69c91-149">-DefaultDocuments</span></span>
<span data-ttu-id="69c91-150">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="69c91-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="69c91-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c91-151">-DefaultProfile</span></span>
<span data-ttu-id="69c91-152">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69c91-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c91-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="69c91-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="69c91-154">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="69c91-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="69c91-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="69c91-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="69c91-156">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="69c91-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="69c91-157">-Ftpsstate</span><span class="sxs-lookup"><span data-stu-id="69c91-157">-FtpsState</span></span>
<span data-ttu-id="69c91-158">Defina o valor do estado de FTPS para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69c91-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="69c91-159">Valores permitidos [permitidos | Desativado | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="69c91-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="69c91-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="69c91-160">-HandlerMappings</span></span>
<span data-ttu-id="69c91-161">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="69c91-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="69c91-162">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="69c91-162">-HostNames</span></span>
<span data-ttu-id="69c91-163">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="69c91-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="69c91-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="69c91-165">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="69c91-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="69c91-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="69c91-166">-HttpsOnly</span></span>
<span data-ttu-id="69c91-167">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="69c91-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="69c91-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="69c91-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="69c91-169">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="69c91-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="69c91-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="69c91-170">-MinTlsVersion</span></span>
<span data-ttu-id="69c91-171">A versão mínima do TLS necessária para solicitações SSL.</span><span class="sxs-lookup"><span data-stu-id="69c91-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="69c91-172">Valores permitidos [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="69c91-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="69c91-173">-Nome</span><span class="sxs-lookup"><span data-stu-id="69c91-173">-Name</span></span>
<span data-ttu-id="69c91-174">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-174">WebApp Name</span></span>

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

### <span data-ttu-id="69c91-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="69c91-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="69c91-176">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="69c91-176">Net Framework Version</span></span>

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

### <span data-ttu-id="69c91-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="69c91-177">-NumberOfWorkers</span></span>
<span data-ttu-id="69c91-178">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="69c91-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="69c91-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="69c91-179">-PhpVersion</span></span>
<span data-ttu-id="69c91-180">Versão do php</span><span class="sxs-lookup"><span data-stu-id="69c91-180">Php Version</span></span>

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

### <span data-ttu-id="69c91-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="69c91-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="69c91-182">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="69c91-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="69c91-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c91-183">-ResourceGroupName</span></span>
<span data-ttu-id="69c91-184">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69c91-184">Resource Group Name</span></span>

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

### <span data-ttu-id="69c91-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="69c91-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="69c91-186">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="69c91-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="69c91-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-187">-WebApp</span></span>
<span data-ttu-id="69c91-188">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-188">WebApp Object</span></span>

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

### <span data-ttu-id="69c91-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="69c91-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="69c91-190">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="69c91-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="69c91-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c91-191">CommonParameters</span></span>
<span data-ttu-id="69c91-192">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c91-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c91-193">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69c91-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c91-194">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69c91-194">INPUTS</span></span>

### <span data-ttu-id="69c91-195">System. Int32</span><span class="sxs-lookup"><span data-stu-id="69c91-195">System.Int32</span></span>

### <span data-ttu-id="69c91-196">System. String</span><span class="sxs-lookup"><span data-stu-id="69c91-196">System.String</span></span>

### <span data-ttu-id="69c91-197">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="69c91-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="69c91-198">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69c91-198">OUTPUTS</span></span>

### <span data-ttu-id="69c91-199">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="69c91-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="69c91-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69c91-200">NOTES</span></span>
<span data-ttu-id="69c91-201">Abaixo o cmdlet fornecido vai ajudá-lo a atualizar o Azure Web App para o **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="69c91-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="69c91-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-Propertyobject $PropertiesObject-ResourceGroupName "Default-Web-Oesteus"-ResourceType Microsoft. Web/sites/config-resourceName "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="69c91-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="69c91-203">Substitua os valores de Default-Web-Oesteus pelo nome do grupo de recursos do webapp e do ContosoWebApp com o nome do webapp.</span><span class="sxs-lookup"><span data-stu-id="69c91-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="69c91-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69c91-204">RELATED LINKS</span></span>

[<span data-ttu-id="69c91-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="69c91-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="69c91-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="69c91-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="69c91-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="69c91-210">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69c91-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="69c91-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="69c91-211">New-AzResource</span></span>](./New-AzResource.md)
